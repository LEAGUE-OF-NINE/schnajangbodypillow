# leemboos structs but protobuf
notes:
- names are 1:1 from the dump, unless specified otherwise
- be sure to look for comments
- and uh, for enums, lets say i have
    ```
    enum SOMETHING {
        // SOMETHING_WHAT = -1
        SOMETHING_NONE = 0;
        COOL = 1;
    }
    ```

    make sure to remove the SOMETHING_ if you're returning string instead of using enum (this is common)

    i have to add the enum name because protobuf uses cpp's shitty enum scoping

    -1 is returned many times, but you have to use it directly, no enum, cuz protobuf doesnt let u use -1 for enums
