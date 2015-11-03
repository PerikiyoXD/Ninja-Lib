##XJ Ninja Model Defnition

Extension: "*.xj"  
Version: Phantasy Star Online BlueBurst PC  

Not exactly sure how or where the xj format came about, though it seems to be
the format used from Phatasy Star Onlinve Version I&II for Gamecube and onward.
So it could have been a new technique or format that the team picked up when
porting the game to different platoforms. While the format itself presents a
challenge in that there's little to no documentation available for it, the good
news is that it's a pretty straight forward format. It uses mostly 32 bit values,
and 16 bit values only on occasion making the data a lot easier to view. And it
seems that the team took the data directly from the old models and exported it
into the new format without changes to the original data. This means there are
parallels to work with and compare when analyzing this format.

### NJTL Ninja Texture List Defnition

With the exception of a few models, most models start with an NJTL texture list
at the top of the file. The NJTL specification is the same one used in the nj
files, so please refer to "NJ_Format.md" is this directory for that information.


### NJCM Ninja Chunk Model Definition

The NJCM is idenfifier for the Ninja Model Chunk format Sega used to define the
game's 3d objects. It follows the NJTL header, though in some models there is
no NJTL header, in which case it will be at the top of the file.

```
typedef struct {
  char identifier[4];
  dword byte_length;
} IFF_HEADER;
```

The NJCM chunk will start following the IFF header, so either trim the file,
or add the offset of the current position to the pointers. Following that
will be the first entry for the parent node, which uses the following format.

```c_cpp
typedef struct obj {
  Uint32 evalflags;                /* Evaluation method optimization flag */
  NJS_MODEL *model;                /* Model structure pointer */
  Float pos[3];                    /* Parallel motion */
  Angle ang[3];                    /* Rotation */
  Float scl[3];                    /* Scale */
  struct obj *child;               /* Child object pointer */
  struct obj *sibling;             /* Sibling object pointer */
} NJS_OBJECT;
```

The initial object structure of xj starts off identical to its nj counter part.
And also 3d objects, such as the weapons which are in both .nj and .xj format
have the exact same values for eval flags such as [this example](http://pastebin.com/kM89aUFj)
which compares the initial values parsed from the saber nj model from version 2,
to its xj saber model counter part in psobb. After this point, the changes in xj
start to become more apparent.
