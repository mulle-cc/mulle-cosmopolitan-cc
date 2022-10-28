cmake_minimum_required( VERSION 3.0)

project( mulle-cosmopolitan-cc NONE)

set( PROJECT_VERSION "0.0.1")

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


######
#
# must be after CPACK_PACKAGE_VERSION
# include( CMakePackage.cmake)
# include( CPack)
