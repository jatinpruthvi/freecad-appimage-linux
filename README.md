# freecad-appimage-linux
Chunked mirror of the official FreeCAD 1.1.3 Linux x86_64 AppImage, published so
environments that cannot reach GitHub's release-asset CDN can still fetch the
exact upstream bytes over ordinary git transport.
- Upstream release: https://github.com/FreeCAD/FreeCAD/releases/tag/1.1.3
- Upstream asset: FreeCAD_1.1.3-Linux-x86_64-py311.AppImage
- Upstream SHA256 (reassembled): 3a853eb69ee595f779f2255dbf80a765926981d8ff68903cefee4dfb03a8f5ef
- Size: 820795896 bytes
- Split: freecad.part-000 .. freecad.part-008 (8 x 99614720 B + 23878136 B)
The bytes are unmodified upstream bytes; only the file is split. Verify:
    cat freecad.part-000 ... freecad.part-008 > freecad.AppImage
    sha256sum -c FreeCAD_1.1.3-Linux-x86_64-py311.AppImage-SHA256.txt
    sha256sum -c SHA256SUMS
See parts.json for the machine-readable manifest. Do not rename, reorder or
re-upload the chunks for an existing version; consumers pin the digests.
For a new FreeCAD version, add new files with the new version in the name.
Linux x86_64 only; the mirror carries no other platform or architecture.
