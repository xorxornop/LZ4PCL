# LZ4PCL #

A pure C# portable class library (PCL) implementation of high performance LZ4 compression algorithm, with streaming interface (System.IO.Stream derived).

It includes a High Compression (HC) codec variant, which is slower than the standard LZ4 codec, but provides a better compression ratio.

This library targets .NET 4.0, Windows Store, Windows Phone 8, and supports use in Xamarin.Android and Xamarin.iOS, implementations of Mono for mobile devices.

When methods are called, it automatically chooses the 32 or 64-bit word size implementations, whichever is fastest for the operation. This library is optimised for high performance, enabled through use of 'unsafe' code blocks: single-thread speeds of >500 MB/s compression (and faster still decompression) are available with only modest hardware.
Please note, best performance requires compilation under the optional 'unsafe' configuration (_ReleaseWithUnsafe_) that provides a very large performance improvement - this works in almost all environments where PCLs do, with the exception of Silverlight, so there's not much reason not to.


Based on the work of Milosz Krajewski and the orginal algorithm author, Yann Collet. These modifications are released under the Apache License 2.0, as found in LICENSE, and in some code file headers.