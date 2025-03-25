for a in {0..30469..250} 
do 
curl "https://www.arquivoalbertosampaio.org/OAI-PMH/oai/?verb=ListRecords&resumptionToken=aif::::$a" -o "mvnv-$a.xml" 
sleep 1 
done

rg -U '<Bio(?s:.)*?</BiogHist>|<UnitTitle.*?</UnitTitle>' mvnv-*.xml  -o

alguns ARQ recomendados
  Famalicao (Alberto Sampaio)
     https://www.arquivoalbertosampaio.org/OAI-PMH/  (30kdoc)
  Ponte do Lima
     https://pesquisa-arquivo.cm-pontedelima.pt/OAI-PMH/   (50kdoc)
  Guimarães (municipal Alfredo Pimenta)
     https://www.amap.pt/
     https://archeevo.amap.pt/OAI-PMH/             (?200kdoc)
  Leiria
     https://arquivo.cm-leiria.pt/OAI-PMH/    (lento) (11kdoc)
  Almada (?)
     https://apps.cm-almada.pt/arquivohistorico/OAI-PMH/   (? kdoc)
  Vila Franca de Xira
     https://arquivo.cm-vfxira.pt/OAI-PMH/    (92kdoc)
  ADB
     https://perquisa.abd.uminho.pt/OAI-PMH/  (465kdoc)
  Ponte da Barca
     https://arquivo.cmpb.pt/OAI-PMH          (13kdoc)
