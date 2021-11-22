# Problemi nel lanciare Python con Windows 10 1903

Dopo l'aggiornamento a Windows 1903, noto anche come *"May update"* molti utenti Python riferiscono l'impossibilità di lanciare da terminale l'interprete Python. Questo problema è dovuto a una novità introdotta da Microsoft con il suddetto aggiornamento. 
<!--more-->

Con il dichiarato intento di facilitare l'installazione di Python per i neofiti durante l'aggiornamento vengono infatti installati due eseguibili, *python.exe* e *python3.exe* il cui unico scopo è quello di reindirizzare allo store Microsoft da cui è possibile scaricare gratuitamente Python
{{< figure src="/images/posts/programmazione/python-store-windows1903.png" alt="Invocare python in Windows 1903 ha l'unico effetto di avviare lo store" caption="*Se si prova ad avviare Python in Windows 10 v1903 viene in realtà avviato lo store di Windows*">}}

A partire dalla versione 3.7.2 Python è anche disponibile come app per lo store di Windows (anche se rispetto alla versione "tradizionale" ha qualche limitazione non avendo ad esempio permessi di scrittura in cartelle comuni come Temp o nel registro di sistema). Il reindirizzamento avviene tuttavia anche se è già stato precedentemente installato Python con il normale programma d'installazione provocando i problemi riportati.

Per fortuna il problema può essere risolto abbastanza facilmente. È sufficiente avviare l'applicazione di configurazione di Windows 10 cliccando sulla ruota dentata nel menu di start ed entrare nella sezione "App"
{{< figure src="/images/posts/programmazione/app-configurazione-windows10.png" alt="App di configurazione di Windows 10" caption="*L'applicazione di configurazione di Windows 10*">}}

Bisogna poi cliccare sulla voce **"Alias di esecuzione App"**:

{{< figure src="/images/posts/programmazione/app-configurazione-windows10-alias.png" alt="Evidenziata voce alias esecuzione App nella App di configurazione di Windows 10" caption="*Finestra per la configurazione degli alias*">}}

Successivamente è sufficiente disattivare le voci **"Programma di installazione App python.exe"** e **"Programma di installazione App python3.exe"** come mostrato in figura

{{< figure src="/images/posts/programmazione/alias-python.png" alt="Alias da disattivare" caption="*Gli alias da disattivare per poter tornare ad eseguire senza problemi Python dalla console*">}}


Una volta fatto si può chiudere la App di configurazione. D'ora in poi sarà di nuovo possibile invocare l'interprete Python da console senza problemi
