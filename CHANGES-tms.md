# Changes in YAFFS to port it to TMS

## yaffs_tagsmarshall.c

Calling `yaffs_tags_marshall_read()` in `yaffs_tags_marshall_query_block()` should be done through pointer `dev->tagger.read_chunk_tags_fn`.

## yaffs_yaffs2.c

Use `yaffs_sort` macro instead of simple `sort`. Just a naming problem.

## direct/yaffsfs.c

`yaffsfs_readdir` now fills field `d_type` in directory entry structure.

## direct/ydirectenv.h and direct/yportenv.h

Changes in definitions, added tms-specific includes.