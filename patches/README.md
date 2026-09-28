Applied on top of the pinned `src/common-src` submodule before building:

    git -C src/common-src apply ../../patches/0001-common-src-lpp-nas.patch

Check it landed: `grep -c GetAdditionalInformation src/common-src/nas/5gmm-msgs/UlNasTransport.hpp` must print 1.

Without it the AMF builds, registers UEs and drops every LPP container silently.
