STD=
WARN=-Wall
OPT=
DEBUG=
FINAL_CFLAGS=$(STD) $(WARN) $(OPT) $(DEBUG) $(CPPFLAGS) $(CFLAGS)
FINAL_LDFLAGS=$(LDFLAGS) $(DEBUG)

L_CC=$(CXX) $(FINAL_CFLAGS)
L_LD=$(CXX) $(FINAL_LDFLAGS)

L_OBJ=l.o

%.o: %.cpp
	$(L_CC) -c $< -o ../target/$@

clean:
	rm -rf target
	mkdir target

L: $(L_OBJ)
	$(L_LD) -o ../target/$@ ../target/$^ 

all: clean L