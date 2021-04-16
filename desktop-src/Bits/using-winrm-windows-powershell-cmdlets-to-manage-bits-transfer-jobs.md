---
title: Verwenden von WinRM Windows PowerShell-Cmdlets zum Verwalten von BITS-Übertragungsaufträgen
description: Windows-Remoteverwaltung PowerShell-Cmdlets können Background Intelligent Transfer Service (Bits)-Übertragungs Aufträge verwalten.
ms.assetid: 9fbef8a1-ed3f-4277-9a07-ed427f60d7a8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eefd874a1056e959d1516d515891ae216e4aca3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523779"
---
# <a name="using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs"></a>Verwenden von WinRM Windows PowerShell-Cmdlets zum Verwalten von BITS-Übertragungsaufträgen

Windows-Remoteverwaltung PowerShell-Cmdlets können Background Intelligent Transfer Service (Bits)-Übertragungs Aufträge verwalten. Weitere Informationen zur Bits-Remote Verwaltung finden Sie unter [Bits-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider) -und Bits- [Anbieter Klassen]( /previous-versions//dd904507(v=vs.85)).

Die folgenden Beispiele erfordern den [Bits-Anbieter](/previous-versions/windows/desktop/bitsprov/bits-provider). Der Bits-Anbieter ist verfügbar, nachdem der BITS Compact-Server installiert wurde. Informationen zum Installieren des Compact-Servers finden Sie in der Dokumentation zu [BITS Compact Server](bits-compact-server.md) .

1.  Erstellen Sie einen Bits-Übertragungs Auftrag.

    ```PowerShell
    # Get the credentials to connect to the remote client computer
    $cred = Get-Credential
    $result = Invoke-WsmanAction -Action CreateJob –Resourceuri wmi/root/microsoft/bits/BitsClientJob `
    –Valueset @{DisplayName="TestJob"; RemoteUrl="https://Server01/servertestdir/testfile1.txt"; LocalFile="C:\clienttestdir\testfile1.txt";Type=0} `
    –ComputerName Client1  -Credential $cred
    ```

    

    Das [Get-Credential-](/previous-versions//dd315327(v=technet.10)) Cmdlet fordert die Anmelde Informationen des Benutzers auf, um eine Verbindung mit dem Remote Computer herzustellen, und weist die Anmelde Informationen dem $cred-Objekt zu.

    Das " [Aufruf-wsmanaction"-](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1) Cmdlet erstellt den Bits-Übertragungs Auftrag auf CLIENT1, indem eine Instanz der Klasse " [bitsclientjob](/previous-versions/windows/desktop/legacy/dd904502(v=vs.85)) " erstellt und die in dem *valueset* -Parameter definierten Informationen in der Hash Tabelle verwendet werden. Der *valueset* -Parameter gibt die Informationen an, die erforderlich sind, um die Parameter der Methode " [kreatejob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) " aufzufüllen. Im vorherigen Beispiel hat der Benutzer den *Typparameter* auf 0 (Download) festgelegt. Der Benutzer gibt auch den Namen der Remote Dateien und lokalen Dateien für den Download Auftrag an. Weitere Informationen zum Erstellen von Bits-Übertragungs Aufträgen und ausführliche Informationen zu Parametern finden Sie unter Methode " [kreatejob](/previous-versions/windows/desktop/bitsprov/createjob-bitsclientjob) ".

    Das " [Aufruf-wsmanaction"-](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet weist das Ergebnis der $Result Variablen zu.

    > [!Note]  
    > Das Zeichen mit einem Doppel Akzent ( \` ) wird verwendet, um einen Zeilenumbruch anzugeben.

     

2.  Legen Sie die Priorität des Bits-Übertragungs Auftrags fest.

    ```PowerShell
    Set-WsmanInstance  -ResourceURI  wmi/root/microsoft/bits/BitsClientJob -SelectorSet @{JobId=$result.JobId} `
    -ValueSet @{Priority=0} –ComputerName Client1  -Credential $cred
    ```

    

    Das [Set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true) -Cmdlet ändert die neue Bits-Übertragungs Auftrags Priorität in 0 (**BG \_ Job \_ priority \_ Vordergrund**). Weitere Informationen zu den Prioritätsstufen finden Sie unter der [**BG- \_ Auftrags \_ Prioritäts**](/windows/desktop/api/Bits/ne-bits-bg_job_priority) -Enumeration.

3.  Setzen Sie den Bits-Übertragungs Auftrag fort.

    ```PowerShell
    Invoke-WsmanAction -Action SetJobState -ResourceUri wmi/root/microsoft/bits/BitsClientJob  -selectorset @{JobId=$result.JobId}  `
    -valueset @{JobState= 2} –ComputerName Client1  -Credential $cred
    ```

    

    Das " [Aufruf-wsmanaction"-](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) Cmdlet ruft die [setjobstate](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) -Methode auf, mit der der Auftragsstatus auf 2 festgelegt wird (Fortsetzen des Auftrags).

4.  Verwalten des Bits-Übertragungs Auftrags.

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

    

    Das vorherige Beispiel ist ein Skript, mit dem der Status des Auftrags abgerufen und eine Aktion basierend auf dem Status ausgeführt wird. Die folgenden Aktionen sind möglich:

    -   Wenn $result. Der Status ist 4 (**Fehler des BG- \_ Auftrags \_ Zustands \_**), das [Aufruf-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) -Cmdlet ruft die [setjobstate](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) -Methode auf und bricht den Auftrag ab.
    -   Wenn $result. Der Status ist 5 (ein **\_ \_ \_ vorübergehender \_ Fehler des BG-Auftrags Zustands**), das Cmdlet " [Aufruf-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) " Ruft die Methode " [setjobstate](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) " auf und bricht den Auftrag ab.
    -   Wenn $result. Der Status ist 6 (der **BG- \_ Auftrags \_ Status wurde \_ übertragen**), das Cmdlet " [Aufruf-wsmanaction](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true) " Ruft die [setjobstate](/previous-versions/windows/desktop/bitsprov/setjobstate-bitsclientjob) -Methode auf und legt den Status auf "abgeschlossen" fest

    Weitere Informationen zu Auftrags Zuständen finden Sie unter der [**BG- \_ Auftrags \_ Status**](/windows/desktop/api/Bits/ne-bits-bg_job_state) -Enumeration.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

["Aufrufen-wsmanaction"](/powershell/module/Microsoft.WsMan.Management/Invoke-WSManAction?view=powershell-5.1&preserve-view=true)
</dt> <dt>

[Set-wsmaninstance](/powershell/module/Microsoft.WsMan.Management/Set-WSManInstance?view=powershell-5.1&preserve-view=true)
</dt> </dl>

 

 
