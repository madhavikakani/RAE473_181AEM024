# RAE473_181AEM024
# DISTRIBUTED SYSTEMS AND THEIR FEATURES

## CASE-1
   ##### Solution
   The client and the server computers may have different hardware but are conected to the internet- therefore we have to deal with differences of representation of data items in request and reply messages from clients to objects. A common standard will be defined for each type of data item that must be transmitted between the object and its clients.
    The computers(client and the server) may run different operating systems, therefore we need to deal with different operations to send and receive messages or to express invocations. Thus at the C++ level a common operation would be used which will be translated to the particular operation according to the operating system it runs on. We have programming languages C++, which use different representations for data structures such as strings, arrays, records. A common standard will be defined for each type of data structure that must be transmitted between the object and its clients and a way of translating between that data structure and each of the languages. We may have different implementors and they will need to agree on the common standards mentioned above and to document them.
    

## CASE-2
   ##### Solution
   As mentioned above the standards must already have been agreed for the distributed system and to add the BLOB object to an existing open distributed system.
     1) Ihe distributed system uses a common set of communication protocols probably the Internet protocols.
     2) It uses an defined standard for representing data items to deal with heterogeneity of hardware.
     3) It uses a common standard for message passing operations.
     4) It uses a language independent standard for representing data structures.
  For the open distributed system the standards must have been agreed and documented before the BLOB object was implemented. The implementors must conform to those standards. In addition, the interface to the BLOB object must be published so that when it is added to the system, both existing and new clients will be able to access it. The publication of the standards allows parts of the system to be implemented by different vendors and to work together.
  
  
## CASE-3
   ##### Solution
   Each request to access a protected operation must include the identity of the user making the request. The problems are:
  (a)defining the identities of the users. Using these identities in the list of users who are allowed to access the protected operations at the implementation of the BLOB object. And in the request messages.
  (b)ensuring that the identity supplied comes from the user it purports to be and not some other user pretending to be that user.
  (c)preventing other users from replaying or tampering with the request messages of legitimate users.
  (d)the information returned as the result of a protected operation must be hidden from unauthorised users. This means that the messages containing the information must be encrypted in case they are intercepted by unauthorised users.
