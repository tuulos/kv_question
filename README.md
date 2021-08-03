# kv_question

Your job is to build a simple key-value server. To make the task easier, the server only serves **read-only** data that is provided in a separate file. The data doesn't need to be mutated in any way by the server. Clients need to be able to contact the server over network (you can choose the protocol), send a query containing a key, and the server will answer with the corresponding value from the dataset, if the given key exists.

The key-value data is provided in the following format:
```
3479d894-3271-4935-88cf-a06f3cbb80a5 this is a value
f8a24bb8-eff8-41dc-929b-10b4c3e49e05 1234
0cdfafb5-edb4-48a6-a7ec-5b1a75831f91 here is another value
```
The first column contains the key which is always a valid [UUID (version 4)](https://en.wikipedia.org/wiki/Universally_unique_identifier#Version_4_(random)). A single space chacterter separates the key from the value that is the rest of the line until a newline (`\n`) character. You can use an example data file stored in this repository, `example.data`, for testing.

In addition to implementing the server, provide an example how a client can request data from the server. The client will provide only a key, e.g. `f8a24bb8-eff8-41dc-929b-10b4c3e49e05`, and the server needs to provide the corresponding value in the response, in this case, `1234`.

You can implement the server and the example client as you see fit. **Important:** you should be able to explain how your system works in detail and answer follow up questions like these:

 - How much data can your server handle? How could you improve it so it can handle even larger datasets?
 - How many milliseconds it takes for the client to get a response on average? How could you improve the latency?
 - What are some failure patterns that you can anticipate?

Note that while you are allowed to use external libraries as a part of your solution, you should be prepared to explain in detail how these libraries work internally. If you are unsure about their internals, it is better to avoid using them and go with a simpler, more understandable approach instead.

Also, while we care about latency and performance, this is not about creating fastest implementation in terms of absolute milliseconds and requests per second. It is perfectly okay to use a high level language like Python; this is not a language benchmark.

Please don't spend more than 1-2 hours of your time. Rather than spending more time in improving your solution, be prepared to have a deep technical discussion about possible improvements and their relative pros and cons.
