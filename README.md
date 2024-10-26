# limbus structs but protobuf
notes:
- names are 1:1 from the dump, unless specified otherwise
- be sure to look for comments
- and uh, for enums, lets say i have
    ```
    enum SOMETHING {
        SOMETHING_NONE = 0;
        COOL = 1;
    }
    ```

    make sure to remove the SOMETHING_ if you're returning string instead of using enum (this is common)

    i have to add the enum name because protobuf uses cpp's shitty enum scoping

    oh and, i commented the ones that are -1 cuz well, again, protobuf lol