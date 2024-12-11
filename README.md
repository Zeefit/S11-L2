 Monitoraggio dei processi e gestione tramite il Registro di Windows

1. Configurazione delle macchine virtuali
- Macchine richieste:  
  - Cyberops Workstation  
  - Security Onion
- **Passaggi iniziali**:  
  - Importare le macchine virtuali.
  - Configurare le schede di rete su **NAT** o **Bridge** per consentire la connessione alla rete esterna.  
  - Avviare le macchine e accedere con le credenziali:  
    - **Utente**: Analyst  
    - **Password**: Cyberops  

2. Modifica delle impostazioni tramite il Registro di Windows
- **Attività sulla macchina locale (facoltativa)**:  
  Utilizzare l'editor del registro (Regedit) per modificare una specifica impostazione.  
  - Avviare Regedit tramite il comando **Win+R** o digitandolo nella barra di ricerca.  
  - Navigare fino alle chiavi di registro:  
    - Per impostazioni di sistema: `HKLM\Software\Microsoft\Windows\CurrentVersion\Run`  
    - Per impostazioni utente: `HKCU\Software\Microsoft\Windows\CurrentVersion\Run`  
  - Cercare e modificare o eliminare voci relative a **NvidiaDisplaysaver** o processi simili.

 3. Utilizzo degli strumenti di monitoraggio
- Aprire **Process Explorer** per identificare i processi configurati per l'avvio automatico.  
- Disabilitare il processo "NvidiaDisplaysaver" in modo che non si avvii più automaticamente.  
- Verificare le modifiche tramite il Registro di Windows e rimuovere definitivamente le chiavi relative.
