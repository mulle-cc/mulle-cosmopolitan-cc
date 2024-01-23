cmake_minimum_required( VERSION 3.0)

project( mulle-cosmopolitan-cc NONE)

set( PROJECT_VERSION "0.0.3")

set( SCRIPTS
   gcc.cosmopolitan
   clang.cosmopolitan
   mulle-clang.cosmopolitan
)

INSTALL( FILES ${SCRIPTS}
PERMISSIONS OWNER_EXECUTE OWNER_WRITE OWNER_READ
            GROUP_EXECUTE GROUP_READ
            WORLD_EXECUTE WORLD_READ
DESTINATION "bin")


#
# with these definitions we provide CC=gcc.musl and COBJC=mulle-clang.musl
# as defaults for mulle-sde builds
#
INSTALL( DIRECTORY definition.cosmopolitan.ALL
         DESTINATION "share/mulle-craft"
         USE_SOURCE_PERMISSIONS
         PATTERN "*._DS_Store" EXCLUDE
)

######
#
# must be after CPACK_PACKAGE_VERSION
# include( CMakePackage.cmake)
# include( CPack)
