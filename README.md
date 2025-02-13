# Concurrent Modification Exception in Kotlin's removeIf
This repository demonstrates a potential issue when using the `removeIf` function on a mutable list in Kotlin.  The `removeIf` function iterates through the list and modifies it simultaneously which can lead to unexpected behavior or `ConcurrentModificationException` in some cases. The solution uses an iterator for safe removal.

## Bug
The original code attempts to remove even numbers from a list.  While it might appear to work in some situations, it's not guaranteed to be thread-safe or reliable due to the potential for concurrent modification.