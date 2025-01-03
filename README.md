# Arjun-s-Cheapest-Travel-Option

In a bustling city, a scholar named Arjun plans to attend an important seminar in Bengaluru. However, he wants to minimize his travel expenses. He has two ways to reach the venue: by taxi or by bus.
The taxi fare works like this: it costs A for the first B kilometers, and C for each kilometer beyond that.
On the other hand, the bus fare is determined by three factors: P as the starting fare, Q as the cost per minute, and R for each kilometer traveled. The bus travels at a speed of S kilometers per minute.
Arjun needs your help to calculate both the taxi and bus fares and determine which option costs less. If both options have the same cost, Arjun prefers to take the taxi. Can you help him make the best decision for his journey?
Input
The first line contains an integer K that denotes the seminar hall distance.
The second line contains the three integers A, B, and C as described above.
The third line contains the four integers P, Q, R, and S as described above.

Constraints
1 ≤ K, A, B, C, P, Q, R, S ≤ 109
Output
Print (without quotes) "Taxi" if Newton visits with a Taxi else prints "Bus".

K = int(input())
A,B,C = map(int, input().split())
S,P,Q,R = map(int,input().split())
taxiFare = (A)+((K-B)*C)
timeInMin = K//S
busFare = P + Q* (timeInMin) + R*K
print("Taxi") if taxiFare <= busFare else print("Bus")
