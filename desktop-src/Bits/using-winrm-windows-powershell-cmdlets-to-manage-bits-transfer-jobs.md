---
title: Verwenden von WinRM Windows PowerShell-Cmdlets zum Verwalten von BITS-Übertragungsaufträgen
description: Windows PowerShell-Cmdlets für die Remoteverwaltung können Background Intelligent Transfer Service (BITS)-Übertragungsaufträge verwalten.
ms.assetid: 9fbef8a1-ed3f-4277-9a07-ed427f60d7a8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f24f4776d8a8431ac8c910fb8145633961bf353721698f8c3e5b4737ee0a1c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004640"
---
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a>Verwenden von WinRM Windows PowerShell-Cmdlets zum Verwalten von BITS-Übertragungsaufträgen

Windows PowerShell-Cmdlets für die Remoteverwaltung können Background Intelligent Transfer Service (BITS)-Übertragungsaufträge verwalten. Weitere Informationen zur BITS-Remoteverwaltung finden Sie unter [BITS-Anbieter-](/previous-versions/windows/desktop/bitsprov/bits-provider) und [BITS-Anbieterklassen.]( /previous-versions//dd904507(v=vs.85))

In den folgenden Beispielen ist der [BITS-Anbieter erforderlich.](/previous-versions/windows/desktop/bitsprov/bits-provider) Der BITS-Anbieter ist verfügbar, nachdem der BITS Compact-Server installiert wurde. Informationen zum Installieren des Compact-Servers finden Sie in der [Dokumentation zu BITS Compact Server.](bits-compact-server.md)

1.  Erstellen Sie einen BITS-Übertragungsauftrag.

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    Das [Cmdlet Get-Credential](/previous-versions//dd315327(v=technet.10)) fordert die Anmeldeinformationen des Benutzers zum Herstellen einer Verbindung mit dem Remotecomputer an und weist die Anmeldeinformationen dem $cred zu.

    Das [Invoke-WsmanAction-Cmdlet](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) erstellt den BITS-Übertragungsauftrag auf Client1, indem es eine Instanz der [BitsClientJob-Klasse](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) erstellt und die Informationen in der Hashtabelle verwendet, die im *Valueset-Parameter definiert* ist. Der *Valueset-Parameter* gibt die Informationen an, die zum Auffüllen der Parameter der [CreateJob-Methode erforderlich](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) sind. Im vorherigen Beispiel legt der Benutzer den *Type-Parameter* auf 0 (Download) fest. Der Benutzer gibt auch den Namen der Remote- und lokalen Dateien für den Downloadauftrag an. Weitere Informationen zum Erstellen von BITS-Übertragungsaufträgen und ausführliche Informationen zu Parametern finden Sie unter [CreateJob-Methode.](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob)

    Das [Invoke-WsmanAction-Cmdlet](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) weist das Ergebnis der $result zu.

    > [!Note]  
    > Das Zeichen mit Dem-Akzent ( \` ) wird verwendet, um einen Zeilenumbruch anzugeben.

     

2.  Legen Sie die Priorität des BITS-Übertragungsauftrags fest.

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    Das [Cmdlet Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) ändert die Neue Bits-Übertragungsauftragspriorität in 0 **(BG JOB PRIORITY \_ \_ \_ FOREGROUND**). Weitere Informationen zu den Prioritätsebenen finden Sie in der [**BG \_ JOB \_ PRIORITY-Enumeration.**](/windows/desktop/api/Bits/ne-bits-bg_job_priority)

3.  Setzen Sie den BITS-Übertragungsauftrag wieder auf.

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    Das [Invoke-WsmanAction-Cmdlet](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) ruft die [SetJobState-Methode](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) auf, die den Auftragsstatus auf 2 (Auftrag fortsetzen) setzt.

4.  Verwalten des BITS-Übertragungsauftrags.

    ```PowerShell
    $IsPprocessing = $TRUE
    while ($IsPprocessing)
    {
        $result = Get-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -selectorset @{JobId = $result.JobId} `
               –ComputerName Client1  -Credential $cred
        if ($result.State -eq 6)
        {

    #Complete the job           
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                          -valueset @{JobState= 1} –ComputerName Client1  -Credential $cred
            "Job Successfully Transferred"
            $IsPprocessing = $FALSE;
        }
        elseif (($result.State -eq 4) -or ($result.State -eq 5))
        {

    #Cancel the job
            "Job is in Error " 
            Invoke-WsmanAction -action SetJobState -resourceuri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
                         -valueset @{JobState= 0} –ComputerName Client1  -Credential $cred
            # You can troubleshoot or delete the job
            $IsPprocessing = $FALSE;
        }
        else
        {
        "Job is processing\n" 
        }

    # Perform other action or poll in a tight loop. This example sleeps for 5 seconds
    sleep 5
    }
    ```

    

    Das vorherige Beispiel ist ein Skript, mit dem sie den Status des Auftrags abruft und basierend auf dem Status eine Aktion ausführen kann. Die folgenden Aktionen sind möglich:

    -   Wenn $result. Der Zustand ist 4 (**BG \_ JOB STATE \_ \_ ERROR),** das [Invoke-WsmanAction-Cmdlet](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) ruft die [SetJobState-Methode](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) auf und bricht den Auftrag ab.
    -   Wenn $result. Der Zustand ist 5 (**BG JOB STATE TRANSIENT \_ \_ \_ \_ ERROR),** das [Invoke-WsmanAction-Cmdlet](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) ruft die [SetJobState-Methode](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) auf und bricht den Auftrag ab.
    -   Wenn $result. Der Zustand ist 6 (**BG \_ JOB STATE \_ \_ TRANSFERD),** das [Invoke-WsmanAction-Cmdlet](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) ruft die [SetJobState-Methode](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) auf und legt den Zustand für den Abschluss fest.

    Weitere Informationen zu Auftragszuständen finden Sie in der [**BG \_ JOB \_ STATE-Enumeration.**](/windows/desktop/api/Bits/ne-bits-bg_job_state)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Invoke-WsmanAction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[Set-WsmanInstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
