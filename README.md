# muon-example-subscriber

A Clojure library designed to demonstrate subscribing to muon event streams using the muon-clojure libary.  At the moment its primarly a 
personal tool to facilitate experimentation at the REPL 

## Usage

This project is in the early stages at the moment it's primary a way to experiment with muon at the REPL.

To get started

1. Ensure you have a photon and rabbitmq instance running
2. Navigate to the root directory of the project
3. at the command line run 'lein repl'
4. Once the clojure repl starts run '(load "subscriber/core")
5. After the message about connecting to rabbit is displayed and the repl returns run '(ns subscriber.core)'
6. To subscribe to the example event stream - the publisher project writes to - run '(subscribe m "test")' N.B. ATM the second parameter is redundant it will however become the stream to subscribe to name.  - This creates an async channel that writes out events as they are created.  (Note at the moment it appears that there is a bug that pervents events being written to and read from a stream at the same time - creating an event from the rest api seams to resolve the deadlock)
7. To get a list of only existing events you can run '(subscribe-cold m "test")' 

your option) any later version.
