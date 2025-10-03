def strStr(haystack: str, needle: str) -> int:
    # Handle the edge case where needle is an empty string
    if not needle:
        return 0
    
    # Get the lengths of haystack and needle
    n, m = len(haystack), len(needle)
    
    # If needle is longer than haystack, it can't be found
    if m > n:
        return -1
    
    # Iterate through haystack to find the first occurrence of needle
    for i in range(n - m + 1):
        if haystack[i:i + m] == needle:
            return i
    
    # Return -1 if needle is not found
    return -1
