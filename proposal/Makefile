main = main
bib = referencias
latex = pdflatex
final = ProyectoCiencias_ForeroRomero
anexo_datos = anexos/anexo_3_carta_datos.pdf
anexo_peder = anexos/LetterCOLCIENCIAS_Norberg.pdf
anexo_desi = anexos/LetterCOLCIENCIAS_Eisenstein.pdf
anexo_paper = anexos/all_papers_uniandes.pdf
anexo_etica_A=anexos/Anexo_ConstitucionComiteEtica.pdf
anexo_etica_B=anexos/Anexo_ActaComiteEtica.pdf


all: $(final).pdf

$(final).pdf: $(main).pdf $(anexo_datos) $(anexo_peder) $(anexo_desi) 
	pdftk $(main).pdf $(anexo_datos) $(anexo_peder) $(anexo_desi) $(anexo_paper) cat output $(final).pdf

$(main).pdf: $(main).tex $(bib).bib 1titulo.tex 2investigadores.tex 3equipo.tex 4antecedentes.tex 5tematica.tex 6resumenejecutivo.tex 7palabrasclave.tex 8planteamientoproblema.tex 9justificacion.tex 10marco.tex 11estadodelarte.tex 12objetivos.tex 13metodologia.tex 14resultados.tex 15productos.tex 16trayectoria.tex 17evaluadores.tex 18cronograma.tex 19impactoambiental.tex 20presupuesto.tex referencias.bib
	pdflatex $(main).tex
	bibtex $(main)
	pdflatex $(main).tex
	pdflatex $(main).tex

zip: 
	zip proyecto_ciencias_ForeroRomero.zip $(final).pdf *.docx 

view: 
	open $(final).pdf

clean:
	rm -f $(main).bbl $(main).aux $(main).pdf $(main).log *~