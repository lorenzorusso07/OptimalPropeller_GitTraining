# GitFlow

Questa è una prova per capire il GitFlow e per utilizzare i comandi git.

<ol>
<li> Da GitHub: creare un fork del progetto per avere una propia repo del progetto.</li>
<li> Da terminale: clonare il progetto con il comando "git clone &#60URL&#62".</li>
<li> Da terminale: passare al branch develop con il comando "git checkout -b develop origin/develop". (Potrebbe non essere necessario se il comando precedente ha gia creato il branch develop. In tal caso git lo segnala dicendo che il branch develop già esiste e quindi basterà passare al branch develop con il comando "git checkout develop")</li>
<li> Da terminale: creare un nuovo branch a partire da quello in cui ci troviamo (develop) con il comando "git checkout -b feature_NuovaFeature" (quindi il nuovo branch si chiamerà feature_NuovaFeature).
  <ul>
<li> Da GitHub: creare un nuovo branch con lo stesso nome di quello creato con git da terminale. NON NECESSARIO se eseguiamo il punto 10!!!</li>
  </ul></li>
<li> Adesso abbiamo creato questo nuovo branch e ci troviamo a lavorare su di esso. Si può fare un controllo per capire che stiamo lavorando in questo branch dando il comando "git status".</li>
<li> Lavoriamo sui file modificandoli con un IDE ad esempio.</li>
<li> Diamo di nuovo il comando "git status" per vedere lo stato dei file modificati. Ci verrà detto che non sono tracciate le modifiche perchè dobbiamo fare l'add del prossimo punto.</li>
<li> Comando "git add file1.cpp file2.cpp" significa che stiamo aggiungendo i file nominati file1.cpp e file2.cpp di cui tracciamo le modifiche o se sono nuovi vengono aggiunti al tracciamento.</li>
<li> Comando "git commit -m "Mettere una breve descrizione della modifica per i file selezionati con il comando add"".</li>
<li> Comando "git push --set-upstream origin feature_NuovaFeature" per inviare il nuovo branch creato su GitHub. </li>
<li> Comando "git push origin feature_NuovaFeature" per inviare le modifiche su GitHub.</li>
</ol>

<b>Qualche chiarimento:</b>
<ul>
<li> Per passare da un branch ad un altro gia esistenti usare il comando "git checkout nomeBranch". </li>
<li>Ogni volta che dobbiamo fare nuove modifiche a dei file dobbiamo sempre assicurarci di essere sul branch giusto con "git status" e dobbiamo sempre fare prima un "git pull" nel caso in cui qualcun altro abbia modificato i file. </li>
 <li>Per vedere in quale branch ci troviamo possiamo anche usare il comando "git branch" il quale ci mostra tutti i branch presenti ed evidenzia quello in cui ci troviamo.</li>
<li> il comando al punto 10 va fatto SOLO LA PRIMA VOLTA che creiamo il branch, per le modifiche successive non sarà più necessario dal momento che il branch sul quale stiamo lavorando sarà già presente su GitHub.</li>
<li> Il comando al punto 9 agisce su tutti i file scelti al punto 8 tramite il comando add. Per cui, per scrivere diverse descrizioni per file diversi bisogna eseguire i punti 8 e 9 in questo modo:
    <ul>
      <li>Comando "git add file1.cpp"</li>
      <li>Comando "git commit -m "Descrizione modifiche al file1.cpp""</li>
      <li>Comando "git add file2.cpp"</li>
      <li>Comando "git commit -m "Descrizione modifiche al file2.cpp""</li>
    </ul>
  </li>
  <li>Una volta fatte tutte le modifiche e verificato che tutto funziona ed è pronto per essere caricato sulla versione ufficiale, bisogna fare (tramite GitHub) una "pull request" dal nostro branch al branch develop inserendo una descrizione di quello che abbiamo fatto (nel nostro caso magari sarà la descrizione del modello che abbiamo implementato).</li>
  <li>Il comando commit al punto 9 può essere dato nella forma seguente per dare un titolo alla modifica ed una breve descrizione di essa:<br>
   git commit -m "Fix computation of the volume for skewed quadrilateral elements."<br>
   \<br>
 -m "If a 2-D quadrilateral element is sufficiently skewed, the volume approximation is not computed properly. This modifies the volume computation to use the base and height of the quadrilateral instead of the base and hypotenuse. This fixes cases where the volume was incorrectly computed to be less than zero. Fixes issue #10."</li>
</ul>
