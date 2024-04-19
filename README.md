from itertools import product

n = int(input())

powers = list(map(int, input().split()))

pairs = list(product(powers, repeat=2))

valid_pairs = []
for pair in pairs:
    if pair[0] * pair[1] == powers[n-1] * powers[n-2]:
        valid_pairs.append(pair)


if valid_pairs:
    print("Yes")
    for pair in valid_pairs:
        print(pair[0], pair[1])
else:
    print("No")
