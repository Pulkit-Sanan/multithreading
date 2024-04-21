## Methodology

1. **Import Libraries:** The code starts by importing necessary libraries such as NumPy, pandas, matplotlib, seaborn, warnings, and multiprocessing.

2. **Get Number of Cores:** It determines the number of CPU cores available on the system using `multiprocessing.cpu_count()`.

3. **Define Matrix Multiplication Function:** The `matrix_multiply` function is defined to perform matrix multiplication using NumPy's `dot` function.

4. **Define Matrix Multiplications Function:** The `perform_matrix_multiplications` function is defined to perform a specified number of matrix multiplications. It generates random matrices of a given size and multiplies them with a constant matrix using the `matrix_multiply` function.

5. **Main Function:** The `main` function is defined to measure the execution time of matrix multiplications using a specified number of threads. It uses Python's `ThreadPoolExecutor` to execute multiple instances of `perform_matrix_multiplications` concurrently with different threads.

6. **Execution:** The code iterates over a range of thread counts, from 1 to the total number of cores, and calls the `main` function for each thread count. It measures and stores the execution time for each thread count.

7. **Result Table:** The execution times for different thread counts are stored in a pandas DataFrame.

8. **Result Graph:** A line plot is created using seaborn to visualize the relationship between the number of threads and the execution time.

## Result Table

The result table shows the number of threads used and the corresponding time taken for matrix multiplications. As the number of threads increases, the execution time generally decreases, up to a certain point. After reaching the optimal number of threads, further increasing the number of threads may not significantly improve performance and could even lead to degradation due to overhead.

## Result Graph

The result graph visualizes the relationship between the number of threads and the execution time. It demonstrates the trend of decreasing execution time with an increasing number of threads, highlighting the potential performance benefits of parallel processing. However, it also indicates that there is an optimal number of threads beyond which further increase does not provide significant improvements in execution time.

![output](https://github.com/Pulkit-Sanan/multithreading/assets/29424760/d2d4d8ab-4589-45c1-9712-fa14feafec1a)

The results can help in determining the optimal number of threads to use for parallel processing tasks, balancing performance gains with resource utilization.
