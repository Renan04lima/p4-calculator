# P4 Calculator
 
  This program implements a simple protocol. It can be carried over Ethernet
  (Ethertype 0x1234).
 
  The Protocol header looks like this:
 
  |       0        |        1       |          2     |         3     |
  |----------------|----------------|----------------|---------------|
  |      P         |       4        |     Version    |     Op        |
  |----------------|----------------|----------------|---------------|
  |                |             Operand A                           |
  |----------------|----------------|----------------|---------------|
  |                |             Operand B                           |
  |----------------|----------------|----------------|---------------|
  |                |             Result                              |
  |----------------|----------------|----------------|---------------|
 
  P is an ASCII Letter 'P' (0x50)
  4 is an ASCII Letter '4' (0x34)
  Version is currently 0.1 (0x01)
  Op is an operation to Perform:
    '+' (0x2b) Result = OperandA + OperandB
    '-' (0x2d) Result = OperandA - OperandB
    '&' (0x26) Result = OperandA & OperandB
    '|' (0x7c) Result = OperandA | OperandB
    '^' (0x5e) Result = OperandA ^ OperandB
 
  The device receives a packet, performs the requested operation, fills in the 
  result and sends the packet back out of the same port it came in on, while 
  swapping the source and destination addresses.
 
  If an unknown operation is specified or the header is not valid, the packet
  is dropped 

# Run Project

- run in super user mode
`./run_task.sh`
- open terminal in prompt of mininet
`xterm h1`
- into the terminal run
`python calc.py`



# Créditos
> Projeto feito durante a aula de Tópicos Avançados de Arquitetura Distribuídas por
  
<br /> 

<div > 

| [<img src="https://avatars.githubusercontent.com/u/48491038?v=4" width=300><br><sub> Renan Oliveira </sub>](https://www.linkedin.com/in/dev-renan/) | ***Caso queira saber mais do projeto ou sobre mim, me chame no LinkedIn*** | 
|---|---|

</div> 
  
<br /> 



