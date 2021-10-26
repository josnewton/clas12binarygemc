#---------------------------------------------------------------------
# Define the C compiler and C flags
#---------------------------------------------------------------------

        CC = cc
        CFLAGS = -c -std=gnu99 

#---------------------------------------------------------------------
# Define rm & mv  so as not to return errors
#---------------------------------------------------------------------

        RM =  rm -f
        MV =  mv -f
        MKDIR = mkdir -p

#---------------------------------------------------
# Program and library names
#---------------------------------------------------

        PROGRAM = cMagTest
        LIBNAME = libcMag.a

#---------------------------------------------------------------------
# The source files that make up the application.
# The library doesn't need main
#---------------------------------------------------------------------

        SRCS = \
	     main.c
            #${CMAG}/cmag/src/maggrid.c\
             ${CMAG}/cmag/src/magfield.c\
             ${CMAG}/cmag/src/magfieldutil.c\
             ${CMAG}/cmag/src/mapcolor.c \
             ${CMAG}/cmag/src/magfielddraw.c \
             ${CMAG}/cmag/src/magfieldio.c \
             ${CMAG}/cmag/src/svg.c \
             ${CMAG}/cmag/src/testdata.c \
             main.c \

        #LIBSRCS = \
              #${CMAG}/cmag/src/maggrid.c\
              ${CMAG}/cmag/src/magfield.c\
              ${CMAG}/cmag/src/magfieldutil.c\
              ${CMAG}/cmag/src/mapcolor.c \
              ${CMAG}/cmag/src/magfielddraw.c \
              ${CMAG}/cmag/src/magfieldio.c \
              ${CMAG}/cmag/src/svg.c \
              ${CMAG}/cmag/src/testdata.c
#---------------------------------------------------------------------
# The object files (via macro substitution)
#---------------------------------------------------------------------

      OBJS = ${SRCS:.c=.o}

#--------------------------------------------------------------------
# required libraries
#--------------------------------------------------------------------

       LIBS = -lm -L/${CMAG}/cmag/lib -lcMag

#---------------------------------------------------------------------
# The includes dir
#---------------------------------------------------------------------

      INCLUDES = -I/${CMAG}/cmag/includes

#---------------------------------------------------------------------
# The object files 
#---------------------------------------------------------------------

      OBJS = ${SRCS:.c=.o}

#--------------------------------------------------------
# Default target
#--------------------------------------------------------

     all:


	$(CC) $(CFLAGS) $(INCLUDES) main.c

	$(CC) -o $(PROGRAM) $(OBJS) $(LIBS) 
	$(MV) $(PROGRAM) ../bin




