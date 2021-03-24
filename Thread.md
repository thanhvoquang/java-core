# Some problem about Java thread

## What is different between Green vs Native thread in Java ?


| FEATURES   | GREEN THREAD (deprecated)                                                                                                                        | NATIVE THREAD                                                                                                                               |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Managed by | JVM without any kind of underlying OS support                                                                                                    | JVM with the help of underlying OS support                                                                                                  |
| Scope      | Implemented at the application level and managed in user space                                                                                   | the OS level (by using OS multithreading API) and managed in kernel space                                                                   |
| Other name | (user-level) threads                                                                                                                             | (kernel-level) threads                                                                                                                      |
| Model      | Only one green thread can be processed at a time (many-to-one model) => run on multi-core processors but cannot take advantage of multiple cores | Many-to-many model => it to take complete advantage of multi-core processors and execute threads on separate individual cores concurrently. |
| Complex    | Synchronization and resource sharing is easier for green threads and hence execution time is also less.                                          | Thread synchronization and resource sharing become complicated. This increases execution time of threads.                                   |



## Reference link

- https://stackoverflow.com/questions/15267269/green-threads-and-native-threads-in-java
- https://docs.oracle.com/cd/E19455-01/806-3461/6jck06gqe/index.html
- https://en.wikipedia.org/wiki/Light-weight_process
- https://www.geeksforgeeks.org/green-vs-native-threads-and-deprecated-methods-in-java/
