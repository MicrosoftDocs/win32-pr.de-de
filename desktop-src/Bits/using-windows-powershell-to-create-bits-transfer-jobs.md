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
# <a name="using-windows-powershell-to-create-bits-transfer-jobs"></a><span data-ttu-id="95d70-103">Erstellen von BITS-Übertragungsaufträgen mithilfe von Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="95d70-103">Using Windows PowerShell to Create BITS Transfer Jobs</span></span>

<span data-ttu-id="95d70-104">Sie können PowerShell-Cmdlets verwenden, um synchrone und asynchrone Background Intelligent Transfer Service (Bits)-Übertragungs Aufträge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="95d70-104">You can use PowerShell cmdlets to create synchronous and asynchronous Background Intelligent Transfer Service (BITS) transfer jobs.</span></span>

<span data-ttu-id="95d70-105">In allen Beispielen in diesem Thema wird das Cmdlet [Start-bitstransfer](/previous-versions//dd347701(v=technet.10)) verwendet.</span><span class="sxs-lookup"><span data-stu-id="95d70-105">All of the examples in this topic use the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="95d70-106">Um das Cmdlet zu verwenden, müssen Sie zuerst das Modul importieren.</span><span class="sxs-lookup"><span data-stu-id="95d70-106">To use the cmdlet, be sure to import the module first.</span></span> <span data-ttu-id="95d70-107">Führen Sie den folgenden Befehl aus, um das Modul zu installieren: Import-Module bitstransfer.</span><span class="sxs-lookup"><span data-stu-id="95d70-107">To install the module, run the following command: Import-Module BitsTransfer.</span></span> <span data-ttu-id="95d70-108">Wenn Sie weitere Informationen benötigen, geben **Sie "Get-Help Start-bitstransfer** " an der PowerShell-Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="95d70-108">For more information, type **Get-Help Start-BitsTransfer** at the PowerShell prompt.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="95d70-109">Wenn Sie [ \* -bitstransfer-](/previous-versions//dd819413(v=technet.10)) Cmdlets von einem Prozess aus verwenden, der in einem nicht interaktiven Kontext (z. b. einem Windows-Dienst) ausgeführt wird, sind Sie möglicherweise nicht in der Lage, Bits-Aufträgen Dateien hinzuzufügen, was zu einem angehaltenen Status führen kann.</span><span class="sxs-lookup"><span data-stu-id="95d70-109">When you use [\*-BitsTransfer](/previous-versions//dd819413(v=technet.10)) cmdlets from within a process that runs in a noninteractive context, such as a Windows service, you may not be able to add files to BITS jobs, which can result in a suspended state.</span></span> <span data-ttu-id="95d70-110">Damit der Auftrag fortgesetzt werden kann, muss die Identität, die zum Erstellen eines Übertragungs Auftrags verwendet wurde, angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="95d70-110">For the job to proceed, the identity that was used to create a transfer job must be logged on.</span></span> <span data-ttu-id="95d70-111">Wenn Sie z. b. einen BITS-Auftrag in einem PowerShell-Skript erstellen, das als Taskplaner Auftrag ausgeführt wurde, wird die Bits-Übertragung nie abgeschlossen, es sei denn, Taskplaner die Task Einstellung "nur ausführen, wenn ein Benutzer angemeldet ist" wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="95d70-111">For example, when creating a BITS job in a PowerShell script that was executed as a Task Scheduler job, the BITS transfer will never complete unless the Task Scheduler's task setting "Run only when user is logged on" is enabled.</span></span>

 

-   [<span data-ttu-id="95d70-112">So erstellen Sie einen synchronen Bits-Übertragungs Auftrag</span><span class="sxs-lookup"><span data-stu-id="95d70-112">To create a synchronous BITS transfer job</span></span>](#to-create-a-synchronous-bits-transfer-job)
-   [<span data-ttu-id="95d70-113">So erstellen Sie einen synchronen Bits-Übertragungs Auftrag mit mehreren Dateien</span><span class="sxs-lookup"><span data-stu-id="95d70-113">To create a synchronous BITS transfer job with multiple files</span></span>](#to-create-a-synchronous-bits-transfer-job-with-multiple-files)
-   [<span data-ttu-id="95d70-114">So erstellen Sie einen synchronen Bits-Übertragungs Auftrag und geben Anmelde Informationen für einen Remote Server an</span><span class="sxs-lookup"><span data-stu-id="95d70-114">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>](#to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server)
-   [<span data-ttu-id="95d70-115">So erstellen Sie einen synchronen Bits-Übertragungs Auftrag aus einer CSV-Datei</span><span class="sxs-lookup"><span data-stu-id="95d70-115">To create a synchronous BITS transfer job from a CSV file</span></span>](#to-create-a-synchronous-bits-transfer-job-from-a-csv-file)
-   [<span data-ttu-id="95d70-116">So erstellen Sie einen asynchronen Bits-Übertragungs Auftrag</span><span class="sxs-lookup"><span data-stu-id="95d70-116">To create an asynchronous BITS transfer job</span></span>](#to-create-an-asynchronous-bits-transfer-job)
-   [<span data-ttu-id="95d70-117">So verwalten Sie PowerShell-Remote Sitzungen</span><span class="sxs-lookup"><span data-stu-id="95d70-117">To manage PowerShell Remote sessions</span></span>](#to-manage-powershell-remote-sessions)
-   [<span data-ttu-id="95d70-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95d70-118">Related topics</span></span>](#related-topics)

## <a name="to-create-a-synchronous-bits-transfer-job"></a><span data-ttu-id="95d70-119">So erstellen Sie einen synchronen Bits-Übertragungs Auftrag</span><span class="sxs-lookup"><span data-stu-id="95d70-119">To create a synchronous BITS transfer job</span></span>


```PowerShell
Start-BitsTransfer -Source https://Server01/serverdir/testfile1.txt `
-Destination C:\clientdir\testfile1.txt
```



> [!Note]  
> <span data-ttu-id="95d70-120">Das Zeichen mit einem Doppel Akzent ( \` ) wird verwendet, um einen Zeilenumbruch anzugeben.</span><span class="sxs-lookup"><span data-stu-id="95d70-120">The grave-accent character (\`) is used to indicate a line break.</span></span>

 

<span data-ttu-id="95d70-121">Im vorherigen Beispiel werden der lokale und der Remote Name der Datei jeweils in den *Quell* -und *Ziel* Parametern angegeben.</span><span class="sxs-lookup"><span data-stu-id="95d70-121">In the preceding example, the local and remote names of the file are specified in the *Source* and *Destination* parameters, respectively.</span></span> <span data-ttu-id="95d70-122">Die Eingabeaufforderung kehrt zurück, nachdem die Dateiübertragung abgeschlossen wurde oder wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="95d70-122">The command prompt returns when the file transfer is complete or when it enters an error state.</span></span>

<span data-ttu-id="95d70-123">Der Standard Übertragungstyp ist herunterladen.</span><span class="sxs-lookup"><span data-stu-id="95d70-123">The default transfer type is Download.</span></span> <span data-ttu-id="95d70-124">Wenn Sie Dateien in einen HTTP-Speicherort hochladen, muss der *TransferType* -Parameter auf Upload festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="95d70-124">When you upload files to an HTTP location, the *TransferType* parameter must be set to Upload.</span></span>

<span data-ttu-id="95d70-125">Da die Parameter Position für das Cmdlet [Start-bitstransfer](/previous-versions//dd347701(v=technet.10)) erzwungen wird, müssen die Parameternamen für die Quell-und Zielparameter nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="95d70-125">Because parameter position is enforced for the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet, the parameter names do not need to be specified for the Source and Destination parameters.</span></span> <span data-ttu-id="95d70-126">Daher kann dieser Befehl wie folgt vereinfacht werden.</span><span class="sxs-lookup"><span data-stu-id="95d70-126">Therefore, this command can be simplified as follows.</span></span>


```PowerShell
Start-BitsTransfer https://Server01/serverdir/testfile1.txt C:\clientdir\testfile1.txt
```



## <a name="to-create-a-synchronous-bits-transfer-job-with-multiple-files"></a><span data-ttu-id="95d70-127">So erstellen Sie einen synchronen Bits-Übertragungs Auftrag mit mehreren Dateien</span><span class="sxs-lookup"><span data-stu-id="95d70-127">To create a synchronous BITS transfer job with multiple files</span></span>


```PowerShell
Start-BitsTransfer -Source C:\clientsourcedir\*.txt `
-Destination c:\clientdir\ -TransferType Download
```



<span data-ttu-id="95d70-128">Im vorherigen Beispiel wird mit dem Befehl [Start-bitstransfer](/previous-versions//dd347701(v=technet.10)) ein neuer Bits-Übertragungs Auftrag erstellt.</span><span class="sxs-lookup"><span data-stu-id="95d70-128">In the preceding example, the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job.</span></span> <span data-ttu-id="95d70-129">Alle Dateien werden diesem Auftrag hinzugefügt und sequenziell auf den Client übertragen.</span><span class="sxs-lookup"><span data-stu-id="95d70-129">All of the files are added to this job and transferred sequentially to the client.</span></span>

> [!Note]  
> <span data-ttu-id="95d70-130">Im Zielpfad dürfen keine Platzhalterzeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95d70-130">The destination path cannot use wildcard characters.</span></span> <span data-ttu-id="95d70-131">Der Zielpfad unterstützt relative Verzeichnisse, Stamm Pfade oder implizite Verzeichnisse (d. h. das aktuelle Verzeichnis).</span><span class="sxs-lookup"><span data-stu-id="95d70-131">The destination path supports relative directories, root paths, or implicit directories (that is, the current directory).</span></span> <span data-ttu-id="95d70-132">Zieldateien können nicht mit einem Platzhalter Zeichen umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="95d70-132">Destination files cannot be renamed by using a wildcard character.</span></span> <span data-ttu-id="95d70-133">Außerdem können http-und HTTPS-URLs nicht mit Platzhaltern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95d70-133">Additionally, HTTP and HTTPS URLs do not work with wildcards.</span></span> <span data-ttu-id="95d70-134">Platzhalter sind nur für UNC-Pfade und lokale Verzeichnisse gültig.</span><span class="sxs-lookup"><span data-stu-id="95d70-134">Wildcards are only valid for UNC paths and local directories.</span></span>

 

## <a name="to-create-a-synchronous-bits-transfer-job-and-specify-credentials-for-a-remote-server"></a><span data-ttu-id="95d70-135">So erstellen Sie einen synchronen Bits-Übertragungs Auftrag und geben Anmelde Informationen für einen Remote Server an</span><span class="sxs-lookup"><span data-stu-id="95d70-135">To create a synchronous BITS transfer job and specify credentials for a remote server</span></span>


```PowerShell
Start-BitsTransfer -DisplayName MyJob -Credential Username\Domain `
-Source https://server01/servertestdir/testfile1.txt -Destination c:\clienttestdir\testfile1.txt `
-ProxyUsage Override -ProxyList @(https://proxy1, 123.24.21.23, proxy3)
```



<span data-ttu-id="95d70-136">Im vorherigen Beispiel erstellt ein Benutzer einen Bits-Übertragungs Auftrag zum Herunterladen einer Datei von einem Server, für den eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="95d70-136">In the preceding example, a user creates a BITS transfer job to download a file from a server that requires authentication.</span></span> <span data-ttu-id="95d70-137">Der Benutzer wird zur Eingabe von Anmelde Informationen aufgefordert, und der *Anmelde Informationen* -Parameter übergibt ein Anmelde Informationen-Objekt an das Cmdlet [Start-bitstransfer](/previous-versions//dd347701(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="95d70-137">The user is prompted for credentials, and the *Credential* parameter passes a credential object to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="95d70-138">Der Benutzer legt einen expliziten Proxy fest, und der Bits-Übertragungs Auftrag verwendet nur die Proxys, die durch den *proxylist* -Parameter definiert werden.</span><span class="sxs-lookup"><span data-stu-id="95d70-138">The user sets an explicit proxy, and the BITS transfer job uses only the proxies that are defined by the *ProxyList* parameter.</span></span> <span data-ttu-id="95d70-139">Der *DisplayName* -Parameter gibt dem Bits-Übertragungs Auftrag einen eindeutigen anzeigen Amen.</span><span class="sxs-lookup"><span data-stu-id="95d70-139">The *DisplayName* parameter gives the BITS transfer job a unique display name.</span></span>

## <a name="to-create-a-synchronous-bits-transfer-job-from-a-csv-file"></a><span data-ttu-id="95d70-140">So erstellen Sie einen synchronen Bits-Übertragungs Auftrag aus einer CSV-Datei</span><span class="sxs-lookup"><span data-stu-id="95d70-140">To create a synchronous BITS transfer job from a CSV file</span></span>


```PowerShell
Import-CSV filelist.txt | Start-BitsTransfer -TransferType Upload
```



> [!Note]  
> <span data-ttu-id="95d70-141">Das Zeichen "" ist ein senkrechter Strich \| .</span><span class="sxs-lookup"><span data-stu-id="95d70-141">The "\|" is the pipe character.</span></span>

 

<span data-ttu-id="95d70-142">Im vorherigen Beispiel erstellt ein Benutzer einen Bits-Übertragungs Auftrag, mit dem mehrere Dateien von einem Client hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="95d70-142">In the preceding example, a user creates a BITS transfer job that uploads multiple files from a client.</span></span> <span data-ttu-id="95d70-143">Das [Import-CSV-](/previous-versions//dd347665(v=technet.10)) Cmdlet importiert die Quell-und Ziel Dateispeicher Orte und leitet Sie an den Befehl [Start-bitstransfer](/previous-versions//dd347701(v=technet.10)) weiter.</span><span class="sxs-lookup"><span data-stu-id="95d70-143">The [Import-CSV](/previous-versions//dd347665(v=technet.10)) cmdlet imports the source and destination file locations and pipes them to the [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command.</span></span> <span data-ttu-id="95d70-144">Mit dem Befehl [Start-bitstransfer](/previous-versions//dd347701(v=technet.10)) wird ein neuer Bits-Übertragungs Auftrag für jede Datei erstellt, die Dateien werden dem Auftrag hinzugefügt und dann sequenziell auf den Server übertragen.</span><span class="sxs-lookup"><span data-stu-id="95d70-144">The [Start-BitsTransfer](/previous-versions//dd347701(v=technet.10)) command creates a new BITS transfer job for each file, adds the files to the job, and then transfers them sequentially to the server.</span></span>

<span data-ttu-id="95d70-145">Der Inhalt der Filelist.txt Datei sollte das folgende Format aufweisen:</span><span class="sxs-lookup"><span data-stu-id="95d70-145">The contents of the Filelist.txt file should be in the following format:</span></span>

``` syntax
Source, Destination
c:\clienttestdir\testfile1.txt, https://server01/servertestdir/testfile1.txt
c:\clienttestdir\testfile2.txt, https://server01/servertestdir/testfile2.txt
c:\clienttestdir\testfile3.txt, https://server01/servertestdir/testfile3.txt
c:\clienttestdir\testfile4.txt, https://server01/servertestdir/testfile4.txt
```

## <a name="to-create-an-asynchronous-bits-transfer-job"></a><span data-ttu-id="95d70-146">So erstellen Sie einen asynchronen Bits-Übertragungs Auftrag</span><span class="sxs-lookup"><span data-stu-id="95d70-146">To create an asynchronous BITS transfer job</span></span>


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



<span data-ttu-id="95d70-147">Im vorherigen Beispiel wurde der Bits-Übertragungs Auftrag der $Job Variablen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="95d70-147">In the preceding example, the BITS transfer job was assigned to the $Job variable.</span></span> <span data-ttu-id="95d70-148">Die Dateien werden sequenziell heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="95d70-148">The files are downloaded sequentially.</span></span> <span data-ttu-id="95d70-149">Nach Abschluss des Übertragungs Auftrags sind die Dateien sofort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="95d70-149">After the transfer job is complete, the files are immediately available.</span></span> <span data-ttu-id="95d70-150">Wenn $Job. jobstate "übertragen" zurückgibt, wird das $Job-Objekt an das [Complete-bitstransfer-]( /previous-versions//dd347701(v=technet.10)) Cmdlet gesendet.</span><span class="sxs-lookup"><span data-stu-id="95d70-150">If $Job.JobState returns "Transferred", the $Job object is sent to the [Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="95d70-151">Wenn $Job. jobstate "Error" zurückgibt, wird das $Job Objekt an das Cmdlet " [Format-List]( /previous-versions//dd347700(v=technet.10)) " gesendet, um die Fehler aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="95d70-151">If $Job.JobState returns "Error", the $Job object is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet to list the errors.</span></span>

## <a name="to-manage-powershell-remote-sessions"></a><span data-ttu-id="95d70-152">So verwalten Sie PowerShell-Remote Sitzungen</span><span class="sxs-lookup"><span data-stu-id="95d70-152">To manage PowerShell Remote sessions</span></span>

<span data-ttu-id="95d70-153">Ab Windows 10, Version 1607, können Sie PowerShell-Cmdlets, BITSAdmin oder andere Anwendungen ausführen, die die Bits- [Schnittstellen](bits-interfaces.md) über eine PowerShell-Remote Befehlszeile verwenden, die mit einem anderen Computer (physisch oder virtuell) verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="95d70-153">Starting with Windows 10, version 1607, you can run PowerShell Cmdlets, BITSAdmin, or other applications that use the BITS [interfaces](bits-interfaces.md) from a PowerShell Remote command line connected to another machine (physical or virtual).</span></span> <span data-ttu-id="95d70-154">Diese Funktion ist nicht verfügbar, wenn Sie eine [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) -Befehlszeile für eine virtuelle Maschine auf demselben physischen Computer verwenden, und Sie ist nicht verfügbar, wenn Sie WinRM-Cmdlets verwenden.</span><span class="sxs-lookup"><span data-stu-id="95d70-154">This capability is not available when using a [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) command line to a virtual machine on the same physical machine, and it is not available when using WinRM cmdlets.</span></span>

<span data-ttu-id="95d70-155">Ein aus einer PowerShell-Remote Sitzung erstellter BITS-Auftrag wird unter dem Benutzerkonto Kontext der Sitzung ausgeführt und wird nur fortgesetzt, wenn mindestens eine aktive lokale Anmelde Sitzung oder eine PowerShell-Remote Sitzung mit diesem Benutzerkonto verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="95d70-155">A BITS Job created from a Remote PowerShell session runs under that session’s user account context and will only make progress when there is at least one active local logon session or Remote PowerShell session associated with that user account.</span></span> <span data-ttu-id="95d70-156">Sie können die persistenten pssessions von PowerShell verwenden, um Remote Befehle auszuführen, ohne dass ein PowerShell-Fenster für jeden Auftrag geöffnet bleiben muss, damit der Fortschritt fortgesetzt wird, wie in [PowerShell-Grundlagen: Remote Verwaltung](https://techgenix.com/remote-management-powershell-part1/)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="95d70-156">You can use PowerShell's persistent PSSessions to run remote commands without the need to keep a PowerShell window open for each job to continue making progress, as described in [PowerShell Basics: Remote Management](https://techgenix.com/remote-management-powershell-part1/).</span></span>

-   <span data-ttu-id="95d70-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) erstellt eine permanente PowerShell-Remote Sitzung.</span><span class="sxs-lookup"><span data-stu-id="95d70-157">[New-PSSession](/powershell/module/microsoft.powershell.core/new-pssession?view=powershell-7&preserve-view=true) creates a persistent Remote PowerShell session.</span></span> <span data-ttu-id="95d70-158">Nach der Erstellung bleiben die PSSession-Objekte auf dem Remote Computer erhalten, bis Sie explizit gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="95d70-158">Once created, the PSSession objects persist in the remote machine until explicitly deleted.</span></span> <span data-ttu-id="95d70-159">Alle Bits-Aufträge, die in einer aktiven Sitzung initiiert werden, übertragen Daten, auch nachdem die Verbindung des Clients mit der Sitzung getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="95d70-159">Any BITS jobs initiated in an active session will make progress transferring data, even after the client has disconnected from the session.</span></span>
-   <span data-ttu-id="95d70-160">[Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) trennt den Client Computer von einer PowerShell-Remote Sitzung, und der Status der Sitzung wird weiterhin vom Remote Computer verwaltet.</span><span class="sxs-lookup"><span data-stu-id="95d70-160">[Disconnect-PSSession](/powershell/module/microsoft.powershell.core/disconnect-pssession?view=powershell-7&preserve-view=true) disconnects the client machine from a Remote PowerShell session and the session’s state continues to be maintained by the remote machine.</span></span> <span data-ttu-id="95d70-161">Am wichtigsten ist, dass die Prozesse der Remote Sitzung weiterhin ausgeführt werden, und BITS-Aufträge werden fortlaufend ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95d70-161">Most importantly, the remote session’s processes will continue executing, and BITS jobs will continue to make progress.</span></span> <span data-ttu-id="95d70-162">Der Client Computer kann auch nach dem Aufruf von Disconnect-PSSession neu gestartet und/oder ausgeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="95d70-162">The client machine can even reboot and/or turn off after calling Disconnect-PSSession.</span></span>
-   <span data-ttu-id="95d70-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) verbindet den Client Computer erneut mit einer aktiven PowerShell-Remote Sitzung.</span><span class="sxs-lookup"><span data-stu-id="95d70-163">[Connect-PSSession](/powershell/module/microsoft.powershell.core/connect-pssession?view=powershell-7&preserve-view=true) re-connects the client machine to an active Remote PowerShell session.</span></span>
-   <span data-ttu-id="95d70-164">[Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) gibt eine PowerShell-Remote Sitzung aus.</span><span class="sxs-lookup"><span data-stu-id="95d70-164">[Remove-PSSession](/powershell/module/microsoft.powershell.core/remove-pssession?view=powershell-7&preserve-view=true) tears down a Remote PowerShell session.</span></span>

<span data-ttu-id="95d70-165">Im folgenden Beispiel wird gezeigt, wie PowerShell Remote verwendet wird, um mit asynchronen Bits-Übertragungs Aufträgen zu arbeiten, sodass der Auftrag fortgesetzt werden kann, auch wenn Sie nicht aktiv mit der Remote Sitzung verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="95d70-165">The example below shows how to use PowerShell Remote to work with asynchronous BITS transfer jobs in a way that allows the job to continue to make progress even when you are not actively connected to the remote session.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="95d70-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95d70-166">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="95d70-167">[Start-bitstransfer](/previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="95d70-167">[Start-BitsTransfer](/previous-versions//dd347701(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="95d70-168">[Complete-bitstransfer]( /previous-versions//dd347701(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="95d70-168">[Complete-BitsTransfer]( /previous-versions//dd347701(v=technet.10))</span></span>
</dt> </dl>

 

 
