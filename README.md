def rec_insertion_sort(arr: list, n: int):
    if n <= 1:
        return
rec_insertion_sort(arr, n - 1)
 last = arr[n - 1]
    j = n - 2
    while j >= 0 and arr[j] > last:
        arr[j + 1] = arr[j]
        j -= 1
    arr[j + 1] = last
lists_to_sort = [
    [4, 3, 5, 1, 2],
    [5, 9, 10, 3, -4, 5, 178, 92, 46, -18, 0, 7],
    [1.1, 1, 0, -1, -1.1, 0.1]
]
for nums in lists_to_sort:
    print("\nOriginal list:")
    print(nums)
    rec_insertion_sort(nums, len(nums))
    print("After applying Recursive Insertion Sort:")
    print(nums)
    
    OUTPUT:
    Original list:
[4, 3, 5, 1, 2]
After applying Recursive Insertion Sort:
[1, 2, 3, 4, 5]

Original list:
[5, 9, 10, 3, -4, 5, 178, 92, 46, -18, 0, 7]
After applying Recursive Insertion Sort:
[-18, -4, 0, 3, 5, 5, 7, 9, 10, 46, 92, 178]

Original list:
[1.1, 1, 0, -1, -1.1, 0.1]
After applying Recursive Insertion Sort:
[-1.1, -1, 0, 0.1, 1, 1.1]

     
