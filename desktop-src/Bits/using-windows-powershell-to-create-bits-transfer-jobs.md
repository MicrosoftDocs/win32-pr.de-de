---
title: Erstellen von BITS-Übertragungsaufträgen mithilfe von Windows PowerShell
description: Sie können PowerShell-Cmdlets verwenden, um synchrone und asynchrone BITS-Übertragungsaufträge (Background Intelligent Transfer Service) zu erstellen.
ms.assetid: 22bcf0d5-36f0-4677-84a7-502b98cfaac2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e939342414d62e4e1af0551318dfec0fb9a5ca59a7e310f13de7b6b67b0440cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118679892"
---
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a>Erstellen von BITS-Übertragungsaufträgen mithilfe von Windows PowerShell

Sie können PowerShell-Cmdlets verwenden, um synchrone und asynchrone BITS-Übertragungsaufträge (Background Intelligent Transfer Service) zu erstellen.

In allen Beispielen in diesem Thema wird das Cmdlet [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) verwendet. Um das Cmdlet zu verwenden, müssen Sie zuerst das Modul importieren. Führen Sie zum Installieren des Moduls den folgenden Befehl aus: Import-Module BitsTransfer. Geben **Sie get-Help Start-BitsTransfer** an der PowerShell-Eingabeaufforderung ein, um weitere Informationen zu erhalten.

> [!IMPORTANT]
>
> Wenn Sie [ \* -BitsTransfer-Cmdlets](/previous-versions//dd819413(v=technet.10)) in einem Prozess verwenden, der in einem nicht interaktiven Kontext ausgeführt wird, z. B. einem Windows Diensts, können Sie bits-Aufträgen möglicherweise keine Dateien hinzufügen, was zu einem angehaltenen Zustand führen kann. Damit der Auftrag fortgesetzt werden kann, muss die Identität angemeldet werden, die zum Erstellen eines Übertragungsauftrags verwendet wurde. Wenn Sie beispielsweise einen BITS-Auftrag in einem PowerShell-Skript erstellen, das als Taskplaner Auftrag ausgeführt wurde, wird die BITS-Übertragung nur abgeschlossen, wenn die Taskeinstellung "Nur ausführen, wenn der Benutzer angemeldet ist" des Taskplaner aktiviert ist.

 

-   [So erstellen Sie einen synchronen BITS-Übertragungsauftrag](#to-create-a-synchronous-bits-transfer-job)
-   [So erstellen Sie einen synchronen BITS-Übertragungsauftrag mit mehreren Dateien](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [So erstellen Sie einen synchronen BITS-Übertragungsauftrag und geben Anmeldeinformationen für einen Remoteserver an](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [So erstellen Sie einen synchronen BITS-Übertragungsauftrag aus einer CSV-Datei](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [So erstellen Sie einen asynchronen BITS-Übertragungsauftrag](#to-create-an-asynchronous-bits-transfer-job)
-   [So verwalten Sie PowerShell-Remotesitzungen](#to-manage-powershell-remote-sessions)
-   [Zugehörige Themen](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a>So erstellen Sie einen synchronen BITS-Übertragungsauftrag


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> Das Akzentzeichen \` () wird verwendet, um einen Zeilenbruch anzugeben.

 

Im vorherigen Beispiel werden die lokalen und Remotenamen der Datei in den Parametern *Quelle* bzw. *Ziel* angegeben. Die Eingabeaufforderung kehrt zurück, nachdem die Dateiübertragung abgeschlossen wurde oder wenn ein Fehler aufgetreten ist.

Der Standardübertragungstyp ist Download. Wenn Sie Dateien an einen HTTP-Speicherort hochladen, muss der *Parameter TransferType* auf Hochladen festgelegt werden.

Da die Parameterposition für das [Cmdlet Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) erzwungen wird, müssen die Parameternamen nicht für die Parameter Source und Destination angegeben werden. Daher kann dieser Befehl wie folgt vereinfacht werden.


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a>So erstellen Sie einen synchronen BITS-Übertragungsauftrag mit mehreren Dateien


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



Im vorherigen Beispiel erstellt der [Befehl Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) einen neuen BITS-Übertragungsauftrag. Alle Dateien werden diesem Auftrag hinzugefügt und sequenziell an den Client übertragen.

> [!Note]  
> Im Zielpfad dürfen keine Platzhalterzeichen verwendet werden. Der Zielpfad unterstützt relative Verzeichnisse, Stammpfade oder implizite Verzeichnisse (das aktuelle Verzeichnis). Zieldateien können nicht mithilfe eines Platzhalterzeichens umbenannt werden. Darüber hinaus funktionieren HTTP- und HTTPS-URLs nicht mit Platzhaltern. Platzhalter sind nur für UNC-Pfade und lokale Verzeichnisse gültig.

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a>So erstellen Sie einen synchronen BITS-Übertragungsauftrag und geben Anmeldeinformationen für einen Remoteserver an


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



Im vorherigen Beispiel erstellt ein Benutzer einen BITS-Übertragungsauftrag, um eine Datei von einem Server herunterzuladen, der eine Authentifizierung erfordert. Der Benutzer wird zur Eingabe von Anmeldeinformationen aufgefordert, und der *Credential-Parameter* übergibt ein Anmeldeinformationsobjekt an das [Cmdlet Start-BitsTransfer.](/previous-versions//dd347701(v=technet.10)) Der Benutzer legt einen expliziten Proxy fest, und der BITS-Übertragungsauftrag verwendet nur die Proxys, die durch den *ProxyList-Parameter* definiert werden. Der *DisplayName-Parameter* gibt dem BITS-Übertragungsauftrag einen eindeutigen Anzeigenamen.

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a>So erstellen Sie einen synchronen BITS-Übertragungsauftrag aus einer CSV-Datei


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> "" \| ist das Pipezeichen.

 

Im vorherigen Beispiel erstellt ein Benutzer einen BITS-Übertragungsauftrag, der mehrere Dateien von einem Client hochlädt. Das Cmdlet [Import-CSV](/previous-versions//dd347665(v=technet.10)) importiert die Quell- und Zieldateispeicherorte und überleitet sie an den Befehl [Start-BitsTransfer.](/previous-versions//dd347701(v=technet.10)) Der Befehl [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) erstellt einen neuen BITS-Übertragungsauftrag für jede Datei, fügt die Dateien dem Auftrag hinzu und überträgt sie dann sequenziell auf den Server.

Der Inhalt der Filelist.txt-Datei sollte das folgende Format aufweisen:

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a>So erstellen Sie einen asynchronen BITS-Übertragungsauftrag


```PowerShell
$Job = Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip `
       -Destination d:\temp\downloads\ -Asynchronous

while (($Job.JobState -eq "Transferring") -or ($Job.JobState -eq "Connecting")) `
       { sleep 5;} # Poll for status, sleep for 5 seconds, or perform an action.

Switch($Job.JobState)
{
    "Transferred" {Complete-BitsTransfer -BitsJob $Job}
    "Error" {$Job | Format-List } # List the errors.
    default {"Other action"} #  Perform corrective action.
}

```



Im vorherigen Beispiel wurde der BITS-Übertragungsauftrag der $Job Variablen zugewiesen. Die Dateien werden sequenziell heruntergeladen. Nach Abschluss des Übertragungsauftrags sind die Dateien sofort verfügbar. Wenn $Job.JobState "Transferd" zurückgibt, wird das $Job -Objekt an das [Complete-BitsTransfer-Cmdlet]( /previous-versions//dd347701(v=technet.10)) gesendet.

Wenn $Job.JobState "Error" zurückgibt, wird das $Job-Objekt an das [Format-List-Cmdlet]( /previous-versions//dd347700(v=technet.10)) gesendet, um die Fehler aufzulisten.

## <a name="to-manage-powershell-remote-sessions"></a>So verwalten Sie PowerShell-Remotesitzungen

Ab Windows 10 Version 1607 können Sie PowerShell-Cmdlets, BITSAdmin oder andere Anwendungen ausführen, die die [BITS-Schnittstellen](bits-interfaces.md) über eine PowerShell Remote-Befehlszeile verwenden, die mit einem anderen Computer verbunden ist (physisch oder virtuell). Diese Funktion ist nicht verfügbar, wenn Sie eine [PowerShell Direct-Befehlszeile](/virtualization/hyper-v-on-windows/user_guide/vmsession) für einen virtuellen Computer auf demselben physischen Computer verwenden, und sie ist nicht verfügbar, wenn Sie WinRM-Cmdlets verwenden.

Ein BITS-Auftrag, der aus einer Remote-PowerShell-Sitzung erstellt wurde, wird im Benutzerkontokontext dieser Sitzung ausgeführt und wird nur dann ausgeführt, wenn diesem Benutzerkonto mindestens eine aktive lokale Anmeldesitzung oder Remote-PowerShell-Sitzung zugeordnet ist. Sie können die persistenten PSSessions von PowerShell verwenden, um Remotebefehle auszuführen, ohne ein PowerShell-Fenster für jeden Auftrag geöffnet zu lassen, um den Fortschritt fortzusetzen, wie unter [PowerShell-Grundlagen: Remoteverwaltung](https://techgenix.com/remote-management-powershell-part1/)beschrieben.

-   [New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) erstellt eine persistente Remote-PowerShell-Sitzung. Nach der Erstellung werden die PSSession-Objekte auf dem Remotecomputer beibehalten, bis sie explizit gelöscht werden. Alle BITS-Aufträge, die in einer aktiven Sitzung initiiert werden, machen den Fortschritt bei der Übertragung von Daten, auch wenn der Client die Verbindung mit der Sitzung getrennt hat.
-   [Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) trennt den Clientcomputer von einer Remote-PowerShell-Sitzung, und der Sitzungszustand wird weiterhin vom Remotecomputer beibehalten. Am wichtigsten ist, dass die Prozesse der Remotesitzung weiterhin ausgeführt werden und BITS-Aufträge weiterhin Fortschritte machen. Der Clientcomputer kann nach dem Aufruf von Disconnect-PSSession sogar neu gestartet und/oder deaktiviert werden.
-   [Verbinden-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) verbindet den Clientcomputer erneut mit einer aktiven Remote-PowerShell-Sitzung.
-   [Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) löscht eine Remote-PowerShell-Sitzung.

Das folgende Beispiel zeigt, wie PowerShell Remote verwendet wird, um mit asynchronen BITS-Übertragungsaufträgen auf eine Weise zu arbeiten, die es dem Auftrag ermöglicht, den Fortschritt auch dann fortzusetzen, wenn Sie nicht aktiv mit der Remotesitzung verbunden sind.


```PowerShell
# Establish a PowerShell Remote session in Server01 with name 'MyRemoteSession'
New-PSSession -ComputerName Server01 -Name MyRemoteSession -Credential Domain01\User01

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# While running in the context of the PowerShell Remote session, start a new BITS transfer
Start-BitsTransfer -Source https://Server1.TrustedDomain.com/File1.zip -Destination c:\temp\downloads\ -Asynchronous

# Exit the PowerShell Remote session's context
Exit-PSSession

# Disconnect the 'MyRemoteSession' PowerShell Remote session from the current PowerShell window
# After this command, it is safe to close the current PowerShell window and turn off the local machine
Disconnect-PSSession -Name MyRemoteSession


# The commands below can be executed from a different PowerShell window, even after rebooting the local machine
# Connect the 'MyRemoteSession' PowerShell Remote session to the current PowerShell window
Connect-PSSession -ComputerName Server01 -Name MyRemoteSession

# Enter the previously-established session to execute commands
Enter-PSSession -Name MyRemoteSession

# Enumerate active BITS transfers on the remote machine
Get-BitsTransfer

# Manage BITS transfers on the remote machine via Complete-BitsTransfer, Remove-BitsTransfer, etc.

# Exit the PowerShell Remote session's context
Exit-PSSession

# Destroy the 'MyRemoteSession' PowerShell Remote session when no longer needed
Remove-PSSession -Name MyRemoteSession
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))
</dt> <dt>

[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))
</dt> </dl>

 

 
