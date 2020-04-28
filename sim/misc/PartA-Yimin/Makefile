YAS=../yas
YIS=../yis

.SUFFIXES: .ys .yo
.ys.yo:
	$(YAS) $*.ys
	$(YIS) $*.yo

all: sum.yo rsum.yo copy.yo

clean:
	rm -f *.yo
