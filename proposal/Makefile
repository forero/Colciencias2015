main = main
bib = referencias
latex = pdflatex
final = ProyectoCiencias_ForeroRomero
anexo_datos = anexos/Anexo5_DatosPersonales_Ciencias
anexo_letter = anexos/LetterCOLCIENCIAS
anexo3_A = anexos/Anexo3_ProyectosActivosCiencias_Forero.pdf
anexo3_B = anexos/Anexo3_ProyectosActivosCiencias_Gomez.pdf
anexo7 = anexos/Anexo7_Terminos.pdf
anexo_etica_A=anexos/Anexo_ConstitucionComiteEtica.pdf
anexo_etica_B=anexos/Anexo_ActaComiteEtica.pdf
anexo6_A=anexos/Anexo6_PropiedadIntelectual_Forero.pdf
anexo6_B=anexos/Anexo6_PropiedadIntelectual_Gomez.pdf

all: $(final).pdf

$(final).pdf: $(main).pdf $(anexo_datos)_Cahn.pdf $(anexo_letter)_Cahn.pdf $(anexo_datos)_Park.pdf $(anexo_letter)_Park.pdf $(anexo_datos)_Gottloeber.pdf $(anexo_letter)_Gottloeber.pdf $(anexo3_A) $(anexo3_B) $(anexo6_A) $(anexo7) $(anexo_etica_A) $(anexo_etica_B) $(anexo6_B)
	pdftk $(main).pdf $(anexo3_A) $(anexo3_B) $(anexo6_A) $(anexo6_B) $(anexo7) $(anexo_etica_A) $(anexo_etica_B) $(anexo_letter)_Cahn.pdf $(anexo_letter)_Park.pdf $(anexo_letter)_Gottloeber.pdf $(anexo_datos)_Cahn.pdf $(anexo_datos)_Park.pdf $(anexo_datos)_Gottloeber.pdf $(anexo_datos)_Forero.pdf $(anexo_datos)_Gomez.pdf cat output $(final).pdf 

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