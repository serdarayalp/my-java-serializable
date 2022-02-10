# How to read and write Java object to a file

Java object Serialization is an API provided by Java Library stack as a means to serialize Java objects. Serialization is a process to convert objects into a writable byte stream. Once converted into a byte-stream, these objects can be written to a file. The reverse process of this is called de-serialization.

A Java object is serializable if its class or any of its superclasses implement either the java.io.Serializable interface or its subinterface, java.io.Externalizable.

# Writing and Reading objects in Java

The objects can be converted into byte-stream using java.io.ObjectOutputStream. In order to enable writing of objects into a file using ObjectOutputStream, it is mandatory that the concerned class implements Serializable interface as shown in the class definition below.

Reading objects in Java are similar to writing object using ObjectOutputStreamObjectInputStream.

On reading objects, the ObjectInputStream directly tries to map all the attributes into the class into which we try to cast the read object. If it is unable to map the respective object exactly then it throws a ClassNotFound exception.

Let us now understand the writing and reading process using an example. We are using the Person class shown above as an object.