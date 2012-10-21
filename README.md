HyperExpress
============

Offers a simple way to add hypermedia links to your domain models before serializing them to clients.

The main hypermedia link class is Link, which supports 'rel', 'href' and 'type' properties, where:

* rel = the relationship from this object to the referred-to object. See ... for standard 'rel' types.
* href = is the fully-qualified URL to the referred-to object.
* type = the type of the referred-to object.

There are two wrapper classes to assist in attaching Link instances to either your domain/DTO classes or to a collection:

* LinkableObject - which accepts an Object instance (generic) in its constructor. You can attached an arbitrary number of links using the addLink() and setLinks() methods.
* LinkableCollection - which accepts a Collection (also generic) implementor in its constructor.

Both of these objects implement the Linkable interface.

Additionally, there are a couple of helper classes to assist in creating URLs and Links en masse:

* MapStringFormat - which will substitute names in a string with provided values (such as an URL).
* LinkUtils - which will perform operations such as replacing create a Collection of Link instances from a list of IDs and an URL, using the substitution capabilities of MapStringFormat.

Interested in other functionality?  Drop me a line... let's talk!