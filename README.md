def max_subarray_sum(nums):
    if not nums:
        return 0  # or float('-inf'), depending on requirements

    max_current = max_global = nums[0]

    for num in nums[1:]:
        max_current = max(num, max_current + num)
        max_global = max(max_global, max_current)

    return max_global
def sort_words_by_length(words):
    return sorted(words, key=len)
def find_primes_in_range(start, end):
    def is_prime(n):
        if n < 2:
            return False
        for i in range(2, int(n**0.5) + 1):
            if n % i == 0:
                return False
        return True

    primes = [num for num in range(start, end + 1) if is_prime(num)]
    return primes
from collections import Counter

def most_frequent_char(s):
    if not s:
        return None  # or raise ValueError("Input string is empty")
    
    counter = Counter(s)
    most_common = counter.most_common(1)[0]  # Returns a tuple: (char, count)
    return most_common[0]
def are_anagrams(str1, str2):
    # Remove spaces and convert to lowercase for a case-insensitive comparison
    str1 = str1.replace(" ", "").lower()
    str2 = str2.replace(" ", "").lower()
    
    return sorted(str1) == sorted(str2)
people = [
    {"name": "Alice", "age": 30},
    {"name": "Bob", "age": 25},
    {"name": "Charlie", "age": 35}
]

sorted_people = sort_dicts_by_key(people, "age")
print(sorted_people)
