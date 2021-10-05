t1:
	for n in 1 2 3 4 5; do \
		ngram-count -order $$n -lm t1n$$n.txt -text ./Corpus\ Dihana/dihana.entrenamiento1.txt ; \
		ngram -order $$n -lm t1n$$n.txt -ppl ./Corpus\ Dihana/dihana.prueba1.txt > t1p$$n.txt.txt ; \
	done 
t2:
	for n in 3 4 ; do \
		for method in -gt -wbdiscount -kndiscount -ukndiscount; do \
			ngram-count -order $$n -lm t2n$$n$$method.txt -text ./Corpus\ Dihana/dihana.entrenamiento1.txt $$method ; \
			ngram -order $$n -lm t2n$$n$$method.txt -ppl ./Corpus\ Dihana/dihana.prueba1.txt > t2p$$n$$method.txt ; \
		done; \
	done 
t3:
	for n in 3 4 ; do \
		for method in -wbdiscount -kndiscount; do \
			ngram-count -order $$n -lm t3n$$n$$method.txt -text ./Corpus\ Dihana/dihana.entrenamiento1.txt $$method -interpolate ; \
			ngram -order $$n -lm t3n$$n$$method.txt -ppl ./Corpus\ Dihana/dihana.prueba1.txt > t3p$$n$$method.txt ; \
		done; \
	done
t4:
	for n in 3 4 ; do \
		for remove in 1 5 9; do \
			ngram-count -order $$n -lm t4n$$n-r$$remove.txt -text ./Corpus\ Dihana/dihana.entrenamiento1.txt -vocab VocabMajor$$remove.txt ; \
			ngram -order $$n -lm t4n$$n-r$$remove.txt -ppl ./Corpus\ Dihana/dihana.prueba1.txt > t4p$$n$$remove.txt ; \
		done; \
	done 