# Vending-Machine
Newspaper Vending Machine

#Design Specification

1) Assume newspaper cost 15cents
2) The coin accceptor takes only nickels and dimes
3) Exact changes must be provided,The acceptor does not returnextra money
4) Valid combinations including order of coins are one nickel and one dime, three nickels or one one dime and one nickel
5) Two dimes are valid but the acceptors does not return money

#Circuit Requirements

1)When each coin is inserted,a 2-bit signal coin [1:0] is sent to the digital circuit.The Signal is asseretd at the next negative edge of a global clock signal and stays up for exactly 1 clock
cycle.
2)The output of the digital circuit is a single bit.Ecah time the total amount inserted is 15cents or more,an output signal newspaper goes high for exactly one clock cycle and vending and machine door is released
3)A reset signal can be used to rest the finite state machine we assume synchronous reset

#Finite State Machine

We represent the functionality of the digital circuit with a finite state machine.

-> input:2 bit Coin [1:0] = no coin x0=2'b00 , nickel x5=2'b01 , dime x10=2'b10 , dont care=2'b11
->output: 1 bit, newspaper =release door when newspaper = 1'b1
-> states: 4states  , s0=0 cents , s5=5 cents , s10=10 cents and s15=15 cents
