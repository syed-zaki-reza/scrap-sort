# scrap-sort
## “Scrap Sorting: A Unique Approach to Optimization”

In Python, while learning about the default search algorithm (Tim Sort), an interesting idea occurred to me. Tim Sort performs well when dealing with semi-sorted values. I initially thought of partially sorting the data to make it even faster than Tim Sort. However, during some test runs, I noticed that the entire runtime of my approach (which I playfully named “Scrap Sorting”) was twice as long as Tim Sort. Surprisingly, other sorting algorithms were faster.

**Step 1:** Initial Gathering To illustrate the entire process, let’s consider an example. Imagine a reunion event at an old school where a total of 1000 students from school graduating batches 2001 to 2020 are gathered in a disorganized manner on the school field.

**Step 2:** Announcing Lunch Distribution Now, suppose an announcement is made for lunch distribution, instructing students to form a single, continuous line starting with the 2001 batch and proceeding roll-wise up to the 2020 batch. One can easily foresee the significant level of chaos and disorder this would create, as students from different batches and roll numbers attempt to organize themselves in a single line.

**Step 3:** Organizing by Batch and Roll Number Instead, consider a more structured approach. An announcement is made directing all students to proceed to designated rooms (Room No. 01 to 20) based on their batch numbers. Subsequently, students are called to the food booth batch-wise, and within each batch, they are organized roll-wise to collect their lunch. This method ensures a much more orderly and efficient distribution process, minimizing confusion and maintaining a smooth flow.

Scrap Sorting follows a similar pattern. Instead of directly sorting the data, you group it into “scrap” and then re-sort these groups using Tim Sort. Additionally, I am planning to dynamically adjust the scrap size based on the frequency of a specific range of values.

When a ship is dismantled, the resulting metal scraps are meticulously sorted in groups based on their sizes. This systematic approach to categorizing and organizing the metal pieces inspired the concept and name ‘Scrap Sorting’. By drawing parallels to this method, Scrap Sorting aims to efficiently group and sort data elements, ensuring a more streamlined and effective sorting process.
