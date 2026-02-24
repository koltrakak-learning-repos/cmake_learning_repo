# TODO12: Move all the MathFunctions target commands to this CMakeLists.txt.
#         Ensure that all paths are updated to be relative to this new location.

# TODO5: Add a library target called MathFunctions to the project
add_library(MathFunctions)

# TODO6: Add the source and header file located in Step1/MathFunctions to the
#        MathFunctions target, note that the intended way to include the
#        MathFunctions header is:
#          #include <MathFunctions.h>
target_sources(MathFunctions
  PRIVATE
    MathFunctions.cxx

  PUBLIC
    FILE_SET HEADERS
    # BASE_DIRS defaults to the current directory of the CML file.
    # Molto comodo quando abbiamo a che fare con librerie e header file
    # dato che la include directory è proprio quella in cui è presente
    # il file CML.
    # BASE_DIRS
    #   MathFunctions
    FILES
      MathFunctions.h
)
