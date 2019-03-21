# RLP (Recursive Length Prefix) Playground

RLP is like a binary encoding of JSON, if JSON were restricted only to strings and arrays.

The RLP encoding function takes in an item. An item is defined as follows：

    A string (ie. byte array) is an item
    A list of items is an item

The string "dog" = [ 0x83, 'd', 'o', 'g' ]

The list [ "cat", "dog" ] = [ 0xc8, 0x83, 'c', 'a', 't', 0x83, 'd', 'o', 'g' ]

The empty string ('null') = [ 0x80 ]

The empty list = [ 0xc0 ]

The integer 0 = [ 0x80 ]

The encoded integer 0 ('\x00') = [ 0x00 ]

The encoded integer 15 ('\x0f') = [ 0x0f ]

The encoded integer 1024 ('\x04\x00') = [ 0x82, 0x04, 0x00 ]

The set theoretical representation of three, [ [], [[]], [ [], [[]] ] ] = [ 0xc7, 0xc0, 0xc1, 0xc0, 0xc3, 0xc0, 0xc1, 0xc0 ]

nothing to see here...yet
