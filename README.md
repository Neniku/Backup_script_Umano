# Backup_script_Umano
Uno script di backup. Proposta N.3 di fine anno. Proposte del Prof. DMZ


Proposta:
• (difficoltà: umana) realizzazione di un software di backup con Linux; il software effettuerà
un backup in base a cinque diverse informazioni passate alla CLI tramite variabili; la
variabile param1 conterrà un path locale, mentre gli altri parametri, conterranno
rispettivamente:
◦ param2 → un indirizzo IP
◦ param3 → uno username
◦ param4 → una password
◦ param5 → potrà valere ftp oppure smb
Il software provvederà a fare una copia ricorsiva di tutto ciò che c’è sotto la directory
param1 dell’host Linux, archiviando i dati in uno o più file (.zip o altro standard di archiviazione
estraibile nativamente anche da Windows) a seconda delle dimensioni del backup; l’archivio,
successivamente, dovrà essere depositato via param5 sfruttando i parametri indicati in param2,
param3 e param4; al termine dell’avvenuto upload sul server, il software dovrà eliminare
automaticamente l’archivio rimasto sul client; il software deve loggare anche l’elenco di tutto ciò
che è stato incluso nell’archivio (sostanzialmente l’elenco dei file e delle directory salvati
all’interno dell’archivio), e tale elenco dovrà essere salvato in un file di testo chiamato diario-
backup.log, che verrà inviato via email al sysadmin al termine del backup.

• (difficoltà: cyborg) modifica il software di backup descritto nel punto precedente in modo
tale che l’archivio venga crittografato in automatico utilizzando cifratura simmetrica e
applicando una password complessa secondo uno schema definito da te; inoltre, il
software depositerà l’archivio di backup sia su di un server sftp (che accetterà connessioni
ssh dai client solo tramite chiavi crittografiche ECC) che su di un server SMB (le
connessioni SMB tra i client e il server SMB dovranno esssere firmate digitalmente);
l’accesso al server di backup dovrà avvenire solo da un indirizzo IP specifico, tutti gli altri
dispositivi e/o workstation sulla sottorete potranno pingare il server di backup ma non
raggiungere i suoi servizi se non dall’ora X all’ora Y (range orari a tua discrezione), in cui il
backup potrà effettivamente partire.
