# -*- coding:utf-8 -*-
from typing import List
from itertools import permutations

operations = {
    '+': lambda x, y: x + y,
    '-': lambda x, y: x - y,
    '*': lambda x, y: x * y,
    '/': lambda x, y: x / y
}

delta = 0.000001

results = []


def calculate_24(nums: List[float], target: float, result: str):
    if len(nums) == 1:
        if abs(nums[0] - target) < delta:
            results.append(result[1:])
        return

    for ops_name, op in operations.items():
        new_num = op(nums[0], nums[1])
        calculate_24([new_num] + nums[2:], target, result + ' ' + str(nums[0]) + ops_name + str(nums[1]))


for i in permutations([3, 5, 2, 1]):
    calculate_24(list(i), 24, '')

print(results)
