---
title: Erstellen von BITS-Übertragungsaufträgen mithilfe von Windows PowerShell
description: Sie können PowerShell-Cmdlets verwenden, um synchrone und asynchrone Background Intelligent Transfer Service (Bits)-Übertragungs Aufträge zu erstellen.
ms.assetid: 22bcf0d5-36f0-4677-84a7-502b98cfaac2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af4879d1fc8f1b25fa0b1b51816432aad3bed8bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748505"
---
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a>Erstellen von BITS-Übertragungsaufträgen mithilfe von Windows PowerShell

Sie können PowerShell-Cmdlets verwenden, um synchrone und asynchrone Background Intelligent Transfer Service (Bits)-Übertragungs Aufträge zu erstellen.

In allen Beispielen in diesem Thema wird das Cmdlet [Start-bitstransfer](/previous-versions//dd347701(v=technet.10)) verwendet. Um das Cmdlet zu verwenden, müssen Sie zuerst das Modul importieren. Führen Sie den folgenden Befehl aus, um das Modul zu installieren: Import-Module bitstransfer. Wenn Sie weitere Informationen benötigen, geben **Sie "Get-Help Start-bitstransfer** " an der PowerShell-Eingabeaufforderung ein.

> [!IMPORTANT]
>
> Wenn Sie [ \* -bitstransfer-](/previous-versions//dd819413(v=technet.10)) Cmdlets von einem Prozess aus verwenden, der in einem nicht interaktiven Kontext (z. b. einem Windows-Dienst) ausgeführt wird, sind Sie möglicherweise nicht in der Lage, Bits-Aufträgen Dateien hinzuzufügen, was zu einem angehaltenen Status führen kann. Damit der Auftrag fortgesetzt werden kann, muss die Identität, die zum Erstellen eines Übertragungs Auftrags verwendet wurde, angemeldet sein. Wenn Sie z. b. einen BITS-Auftrag in einem PowerShell-Skript erstellen, das als Taskplaner Auftrag ausgeführt wurde, wird die Bits-Übertragung nie abgeschlossen, es sei denn, Taskplaner die Task Einstellung "nur ausführen, wenn ein Benutzer angemeldet ist" wird aktiviert.

 

-   [So erstellen Sie einen synchronen Bits-Übertragungs Auftrag](#to-create-a-synchronous-bits-transfer-job)
-   [So erstellen Sie einen synchronen Bits-Übertragungs Auftrag mit mehreren Dateien](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [So erstellen Sie einen synchronen Bits-Übertragungs Auftrag und geben Anmelde Informationen für einen Remote Server an](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [So erstellen Sie einen synchronen Bits-Übertragungs Auftrag aus einer CSV-Datei](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [So erstellen Sie einen asynchronen Bits-Übertragungs Auftrag](#to-create-an-asynchronous-bits-transfer-job)
-   [So verwalten Sie PowerShell-Remote Sitzungen](#to-manage-powershell-remote-sessions)
-   [Zugehörige Themen](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a>So erstellen Sie einen synchronen Bits-Übertragungs Auftrag


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> Das Zeichen mit einem Doppel Akzent ( \` ) wird verwendet, um einen Zeilenumbruch anzugeben.

 

Im vorherigen Beispiel werden der lokale und der Remote Name der Datei jeweils in den *Quell* -und *Ziel* Parametern angegeben. Die Eingabeaufforderung kehrt zurück, nachdem die Dateiübertragung abgeschlossen wurde oder wenn ein Fehler aufgetreten ist.

Der Standard Übertragungstyp ist herunterladen. Wenn Sie Dateien in einen HTTP-Speicherort hochladen, muss der *TransferType* -Parameter auf Upload festgelegt werden.

Da die Parameter Position für das Cmdlet [Start-bitstransfer](/previous-versions//dd347701(v=technet.10)) erzwungen wird, müssen die Parameternamen für die Quell-und Zielparameter nicht angegeben werden. Daher kann dieser Befehl wie folgt vereinfacht werden.


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a>So erstellen Sie einen synchronen Bits-Übertragungs Auftrag mit mehreren Dateien


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



Im vorherigen Beispiel wird mit dem Befehl [Start-bitstransfer](/previous-versions//dd347701(v=technet.10)) ein neuer Bits-Übertragungs Auftrag erstellt. Alle Dateien werden diesem Auftrag hinzugefügt und sequenziell auf den Client übertragen.

> [!Note]  
> Im Zielpfad dürfen keine Platzhalterzeichen verwendet werden. Der Zielpfad unterstützt relative Verzeichnisse, Stamm Pfade oder implizite Verzeichnisse (d. h. das aktuelle Verzeichnis). Zieldateien können nicht mit einem Platzhalter Zeichen umbenannt werden. Außerdem können http-und HTTPS-URLs nicht mit Platzhaltern verwendet werden. Platzhalter sind nur für UNC-Pfade und lokale Verzeichnisse gültig.

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a>So erstellen Sie einen synchronen Bits-Übertragungs Auftrag und geben Anmelde Informationen für einen Remote Server an


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



Im vorherigen Beispiel erstellt ein Benutzer einen Bits-Übertragungs Auftrag zum Herunterladen einer Datei von einem Server, für den eine Authentifizierung erforderlich ist. Der Benutzer wird zur Eingabe von Anmelde Informationen aufgefordert, und der *Anmelde Informationen* -Parameter übergibt ein Anmelde Informationen-Objekt an das Cmdlet [Start-bitstransfer](/previous-versions//dd347701(v=technet.10)) . Der Benutzer legt einen expliziten Proxy fest, und der Bits-Übertragungs Auftrag verwendet nur die Proxys, die durch den *proxylist* -Parameter definiert werden. Der *DisplayName* -Parameter gibt dem Bits-Übertragungs Auftrag einen eindeutigen anzeigen Amen.

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a>So erstellen Sie einen synchronen Bits-Übertragungs Auftrag aus einer CSV-Datei


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> Das Zeichen "" ist ein senkrechter Strich \| .

 

Im vorherigen Beispiel erstellt ein Benutzer einen Bits-Übertragungs Auftrag, mit dem mehrere Dateien von einem Client hochgeladen werden. Das [Import-CSV-](/previous-versions//dd347665(v=technet.10)) Cmdlet importiert die Quell-und Ziel Dateispeicher Orte und leitet Sie an den Befehl [Start-bitstransfer](/previous-versions//dd347701(v=technet.10)) weiter. Mit dem Befehl [Start-bitstransfer](/previous-versions//dd347701(v=technet.10)) wird ein neuer Bits-Übertragungs Auftrag für jede Datei erstellt, die Dateien werden dem Auftrag hinzugefügt und dann sequenziell auf den Server übertragen.

Der Inhalt der Filelist.txt Datei sollte das folgende Format aufweisen:

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a>So erstellen Sie einen asynchronen Bits-Übertragungs Auftrag


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



Im vorherigen Beispiel wurde der Bits-Übertragungs Auftrag der $Job Variablen zugewiesen. Die Dateien werden sequenziell heruntergeladen. Nach Abschluss des Übertragungs Auftrags sind die Dateien sofort verfügbar. Wenn $Job. jobstate "übertragen" zurückgibt, wird das $Job-Objekt an das [Complete-bitstransfer-]( /previous-versions//dd347701(v=technet.10)) Cmdlet gesendet.

Wenn $Job. jobstate "Error" zurückgibt, wird das $Job Objekt an das Cmdlet " [Format-List]( /previous-versions//dd347700(v=technet.10)) " gesendet, um die Fehler aufzulisten.

## <a name="to-manage-powershell-remote-sessions"></a>So verwalten Sie PowerShell-Remote Sitzungen

Ab Windows 10, Version 1607, können Sie PowerShell-Cmdlets, BITSAdmin oder andere Anwendungen ausführen, die die Bits- [Schnittstellen](bits-interfaces.md) über eine PowerShell-Remote Befehlszeile verwenden, die mit einem anderen Computer (physisch oder virtuell) verbunden ist. Diese Funktion ist nicht verfügbar, wenn Sie eine [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) -Befehlszeile für eine virtuelle Maschine auf demselben physischen Computer verwenden, und Sie ist nicht verfügbar, wenn Sie WinRM-Cmdlets verwenden.

Ein aus einer PowerShell-Remote Sitzung erstellter BITS-Auftrag wird unter dem Benutzerkonto Kontext der Sitzung ausgeführt und wird nur fortgesetzt, wenn mindestens eine aktive lokale Anmelde Sitzung oder eine PowerShell-Remote Sitzung mit diesem Benutzerkonto verknüpft ist. Sie können die persistenten pssessions von PowerShell verwenden, um Remote Befehle auszuführen, ohne dass ein PowerShell-Fenster für jeden Auftrag geöffnet bleiben muss, damit der Fortschritt fortgesetzt wird, wie in [PowerShell-Grundlagen: Remote Verwaltung](https://techgenix.com/remote-management-powershell-part1/)beschrieben.

-   [New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) erstellt eine permanente PowerShell-Remote Sitzung. Nach der Erstellung bleiben die PSSession-Objekte auf dem Remote Computer erhalten, bis Sie explizit gelöscht werden. Alle Bits-Aufträge, die in einer aktiven Sitzung initiiert werden, übertragen Daten, auch nachdem die Verbindung des Clients mit der Sitzung getrennt wurde.
-   [Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) trennt den Client Computer von einer PowerShell-Remote Sitzung, und der Status der Sitzung wird weiterhin vom Remote Computer verwaltet. Am wichtigsten ist, dass die Prozesse der Remote Sitzung weiterhin ausgeführt werden, und BITS-Aufträge werden fortlaufend ausgeführt. Der Client Computer kann auch nach dem Aufruf von Disconnect-PSSession neu gestartet und/oder ausgeschaltet werden.
-   [Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) verbindet den Client Computer erneut mit einer aktiven PowerShell-Remote Sitzung.
-   [Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) gibt eine PowerShell-Remote Sitzung aus.

Im folgenden Beispiel wird gezeigt, wie PowerShell Remote verwendet wird, um mit asynchronen Bits-Übertragungs Aufträgen zu arbeiten, sodass der Auftrag fortgesetzt werden kann, auch wenn Sie nicht aktiv mit der Remote Sitzung verbunden sind.


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

[Start-bitstransfer](/previous-versions//dd347701(v=technet.10))
</dt> <dt>

[Complete-bitstransfer]( /previous-versions//dd347701(v=technet.10))
</dt> </dl>

 

 
