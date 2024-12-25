Fast java implementation of the Queue interface using an array.


HOW TO USE:

  Construce with                                                         ArrayQueue<Object> name = new ArrayQueue<>(capacity);
  
  Add to queue with                                                      name.enqueue(object);
  
  Get next element with                                                  Object object = name.dequeue();
  
  Get size with                                                          int size = name.size();
  
  Check if empty with                                                    boolean empty = name.isEmpty(); // same as name.size() == 0
  
  Peek at first element without removing it with                         Object object = name.front();
  
  Check if an element is already in the list (uses .equlas not ==) with  name.contains(object);
  

  IMPLEMENTATION DETAILS:

  headPointer is the index of the next element to be returned form front() or dequeue()
  tailPointer is the index of the last element that was added using enqueue();
  The underlying array only grows when absolutely necessary, so tailPointer can be smaller than headPointer in some cases.
  Any capacity samller than 2 will get clamped to 2.
