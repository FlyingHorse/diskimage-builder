==============
no-final-image
==============

This is a noop element which can be used to indicate to diskimage-builder that
it should not bother creating a final image out of the generated filesystem.
It is useful in cases where an element handles all of the image building
itself, such as ironic-agent or Docker images.  In those cases the final image
normally generated by diskimage-builder is not the desired output, so there's
no reason to spend time creating it.

Elements that wish to behave this way should include this element in their
element-deps file.
