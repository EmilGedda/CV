SRCDIR := ../src
OBJS = main.pdf

CC = latexmk
OPT = -pdf -xelatex

%.pdf: $(SRCDIR)/%.tex
	${CC} ${OPT} $<

watch: OPT := $(OPT) -pvc
watch: fullclean 
	
all pdf watch: $(OBJS) 
	cp $< EmilGedda-CV.pdf

clean:
	$(CC) -f -c $(OBJS)


fullclean:
	$(CC) -f -C $(OBJS) 
	rm -f EmilGedda-CV.pdf
