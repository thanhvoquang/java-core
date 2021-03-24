# java-core

# java-core

What is difffrent Green Thread vs Native Thread ?
[a link](https://github.com/user/repo/blob/branch/other_file.md)

| FEATURES   | GREEN THREAD (deprecated)                                                                                                                           | NATIVE THREAD                                                                                                                                  |
| ---------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| Managed by | JVM without any kind of underlying OS support                                                                                                       | JVM with the help of underlying OS support                                                                                                     |
| Scope      | Implemented at the application level and managed in user space                                                                                      | the OS level (by using OS multithreading API) and managed in kernel space                                                                      |
| Other name | (user-level) threads                                                                                                                                | (kernel-level) threads                                                                                                                         |
| Model      |  [ManyToOne model](https://docs.oracle.com/cd/E19455-01/806-3461/ch2mt-41/index.html) - Only one green thread can be processed at a time: <br/> <ul><li>Context switches all Java threads within one operating system process</li><li>Run on multi-core processors but cannot take advantage of multiple cores</li></ul>  | Many-to-many model <br/> <ul><li>Each Java thread is mapped to one threads library thread (using the operating system threads library)</li><li>it to take complete advantage of multi-core processors</li></ul> |
| Complex    | Synchronization and resource sharing is easier for green threads and hence execution time is also less.                                             | Thread synchronization and resource sharing become complicated. This increases execution time of threads.                                      |
