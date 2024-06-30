# Scrap Sort: An Optimization Technique for Data Sorting

## Introduction

Within the domain of sorting algorithms, Tim Sort stands as a well-established method. Tim Sort demonstrates superior performance when handling semi-sorted datasets. However, an alternative approach ***'Scrap Sort'*** is proposed, aiming to enhance Tim Sort's efficiency by capitalizing on semi-sorted data. Despite the additional time required for Scrap Sorting compared to Tim Sort, it outperforms other renowned sorting algorithms.

## The Concept

Let us elucidate the sorting process through an illustrative example:

1. **Unsorted Structure**: Consider a gathering of thousands of students, representing graduating batches from 2001 to 2020. Initially disorganized, they disperse across a vast field. Now envision arranging them in a line based on their batch year and roll number.

2. **Group Allocation**: Instead of creating a single disorderly line based solely on batch and roll numbers, adopt a structured strategy. Students are directed to designated rooms (e.g., Room No. 01 to 20). Within these rooms, they organize themselves into smaller groups such that smaller groups are made with neighboring roll numbers.

3. **Sorted Assembly**: If our goal is to create a batch year-wise and roll-wise assembly line, we need only sort within each room. This approach minimizes chaos and enhances efficiency.

## The Methodology

Inspired by the meticulous categorization of metal scraps with varying weights and shapes during ship dismantling, Scrap Sorting emerges. Imagine data elements as categorized fragments, each standing alongside its neighboring values. These groups resemble nearly uniform-sized scraps.

- **Efficiency**: Scrap Sorting improves Tim Sort's efficiency by minimizing comparisons.

- **Grouping**: Scraps form a chain of semi-sorted values. Neighboring values exhibit similar and close values.

- **Ranging**: When seeking specific values within a range, Scrap Sorting selectively extracts relevant values. This avoids the need to sort the entire dataset and allows for efficient retrieval of sorted values within specific ranges.


## PseudoCode
```
# Calculate min and max values in the large array
large_array_min_value = calculate_min(large_array)
large_array_max_value = calculate_max(large_array)

# Determine the number of scraps
sturges_num_scraps = calculate_sturges_num_scraps(length(large_array))
if sturges_num_scraps is even:
    sturges_num_scraps += 1

# Calculate scrap size
scrap_size = (large_array_max_value - large_array_min_value) / sturges_num_scraps)

# Create scrap bins
num_scraps = large_array_max_value / scrap_size
scraps = create_empty_scraps(num_scraps)

# Distribute elements into appropriate scrap bins
for element in large_array:
    scrap_index = element / scrap_size
    add_to_scrap(scraps[scrap_index], element)

# Flatten the scraps into a partially sorted array
partially_sorted = flatten_scraps(scraps)

# Sort the partially sorted array
sorted_partially_sorted = tim_sort(partially_sorted)

# Calculate overall time for scrap sorting
overall_time_scrap_sort = calculate_overall_time_scrap_sort()
```