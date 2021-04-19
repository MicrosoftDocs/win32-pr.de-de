---
description: Geplante WMI-Tasks erstellen und erhalten Informationen zu geplanten Tasks. Weitere Beispiele finden Sie im technet scriptcenter unter https://www.microsoft.com/technet .
ms.assetid: 62151fe8-8880-43f2-b456-628bd9c7cc1c
ms.tgt_platform: multiple
title: 'WMI-Tasks: geplante Aufgaben'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4051df4348ee47710b5d2d1f5dcc3f59f607d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360188"
---
# <a name="wmi-tasks-scheduled-tasks"></a><span data-ttu-id="fcabf-104">WMI-Tasks: geplante Aufgaben</span><span class="sxs-lookup"><span data-stu-id="fcabf-104">WMI Tasks: Scheduled Tasks</span></span>

<span data-ttu-id="fcabf-105">Geplante WMI-Tasks erstellen und erhalten Informationen zu geplanten Tasks.</span><span class="sxs-lookup"><span data-stu-id="fcabf-105">WMI scheduled tasks create and get information about scheduled tasks.</span></span> <span data-ttu-id="fcabf-106">Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="fcabf-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="fcabf-107">In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fcabf-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="fcabf-108">Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="fcabf-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="fcabf-109">Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fcabf-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="fcabf-110">**So führen Sie ein Skript aus**</span><span class="sxs-lookup"><span data-stu-id="fcabf-110">**To run a script**</span></span>

1.  <span data-ttu-id="fcabf-111">Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="fcabf-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="fcabf-112">Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="fcabf-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="fcabf-113">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="fcabf-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="fcabf-114">Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="fcabf-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="fcabf-115">Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcabf-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="fcabf-116">Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.</span><span class="sxs-lookup"><span data-stu-id="fcabf-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="fcabf-117">Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an.</span><span class="sxs-lookup"><span data-stu-id="fcabf-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="fcabf-118">Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="fcabf-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="fcabf-119">Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="fcabf-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="fcabf-120">In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="fcabf-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fcabf-121">Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="fcabf-121">How do I...</span></span></th>
<th><span data-ttu-id="fcabf-122">WMI-Klassen oder-Methoden</span><span class="sxs-lookup"><span data-stu-id="fcabf-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fcabf-123">... Erstellen Sie geplante Tasks mithilfe von Skripts?</span><span class="sxs-lookup"><span data-stu-id="fcabf-123">...create scheduled tasks using scripts?</span></span></td>
<td><span data-ttu-id="fcabf-124">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="fcabf-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method.</span></span> <span data-ttu-id="fcabf-125">Wenn Sie Schwierigkeiten haben, diese Aufgabe unter Windows 7 oder höher zu funktionieren, finden Sie weitere Informationen im Abschnitt <strong>Win32_ScheduledJob</strong> Hinweise. wahrscheinlich verhindern Ihre Einstellungen, dass Sie die-Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="fcabf-125">If you are having difficulty making this task work on Windows 7 or later, see the <strong>Win32_ScheduledJob</strong> Remarks section; likely your settings are preventing you from using the class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fcabf-126">VB</span><span class="sxs-lookup"><span data-stu-id="fcabf-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
JobID = &quot;Test&quot;
Set objNewJob = objWMIService.Get(&quot;Win32_ScheduledJob&quot;)
errJobCreate = objNewJob.Create _
    (&quot;Notepad.exe&quot;, &quot;********143000.000000-420&quot;, True , 1 OR 4 OR 16, ,True, JobId) 
If errJobCreate = 0 Then
    WScript.Echo &quot;Job created successfully: &quot; & VBNewLine _
        & &quot;Notepad.exe scheduled to run repeately at 14.30 (2:30 P.M.) PST&quot; & VBNewLine _
        & &quot;on Mon, Wed, and Fri.&quot;
Else
    WScript.Echo &quot;Job not created. Error code = &quot; & errJobCreate
End If</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="fcabf-127">In der Zeichenfolge \* \* \* \* \* \* \* &quot; \* 143000.000000-420 &quot; (wird im <em>StartTime</em> -Parameterwert der <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> -Methode verwendet), &quot; gibt \* \* \* \* \* \* \* \* \* 143000,000000 &quot; an, dass der Task um 14,30 (2:30 Uhr) beginnt und &quot; -420 &quot; die Zeitzone angibt.</span><span class="sxs-lookup"><span data-stu-id="fcabf-127">In the string &quot;\*\*\*\*\*\*\*\*143000.000000-420&quot; (used in the <em>StartTime</em> parameter value of the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method), &quot;\*\*\*\*\*\*\*\*143000.000000&quot; specifies that the task starts at 14.30 (2:30 P.M.) and &quot;-420&quot; specifies the time zone.</span></span> <span data-ttu-id="fcabf-128">Die Zeit Zonennummer ist die aktuelle Abweichung der lokalen Zeit Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="fcabf-128">The time zone number is the current bias of the local time translation.</span></span> <span data-ttu-id="fcabf-129">Die Verschiebung ist der Unterschied zwischen der UTC-Zeit und der Ortszeit.</span><span class="sxs-lookup"><span data-stu-id="fcabf-129">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="fcabf-130">Multiplizieren Sie die Anzahl der Stunden, die Ihre Zeitzone vor oder hinter der Ortszeit (GMT) um 60 liegen soll, um die Verschiebung für Ihre Zeitzone zu berechnen (verwenden Sie eine positive Zahl für die Anzahl von Stunden, wenn Ihre Zeitzone vor GMT liegt, und eine negative Zahl, wenn sich Ihre Zeitzone hinter GMT befindet).</span><span class="sxs-lookup"><span data-stu-id="fcabf-130">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="fcabf-131">Fügen Sie der Berechnung eine zusätzliche 60 hinzu, wenn die Zeitzone die Sommerzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="fcabf-131">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="fcabf-132">Die Pacific Standard Time-Zone beträgt z. b. acht Stunden hinter GMT. Daher entspricht der Bias dem Wert-420 (-8 \* 60 + 60), wenn die Sommerzeit verwendet wird, und-480 (-8 \* 60), wenn die Sommerzeit nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fcabf-132">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="fcabf-133">Sie können auch den Wert der Bias ermitteln, indem Sie die Eigenschaft "Bias" der <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> Klasse Abfragen.</span><span class="sxs-lookup"><span data-stu-id="fcabf-133">You can also determine the value of the bias by querying the bias property of the <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> class.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fcabf-134">... gibt eine Liste aller geplanten Aufgaben auf einem Computer zurück?</span><span class="sxs-lookup"><span data-stu-id="fcabf-134">...return a list of all the scheduled tasks on a computer?</span></span></td>
<td><p><span data-ttu-id="fcabf-135">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> -Klasse.</span><span class="sxs-lookup"><span data-stu-id="fcabf-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class.</span></span> <span data-ttu-id="fcabf-136">Beachten Sie, dass diese Klasse nur Aufträge zurückgeben kann, die entweder mit einem Skript oder mit AT.exe erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fcabf-136">Note that this class can only return jobs that are created using either a script or AT.exe.</span></span> <span data-ttu-id="fcabf-137">Informationen zu Aufträgen, die vom Assistenten für geplante Aufgaben erstellt oder geändert werden, können nicht zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fcabf-137">It cannot return information about jobs that are either created by or modified by the Scheduled Task wizard.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fcabf-138">VB</span><span class="sxs-lookup"><span data-stu-id="fcabf-138">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colScheduledJobs = objWMIService.ExecQuery (&quot;Select * from Win32_ScheduledJob&quot;)
For Each objJob in colScheduledJobs
    Wscript.Echo &quot;Command: &quot; & objJob.Command & VBNewLine _
    & &quot;Days Of Month: &quot; & objJob.DaysOfMonth & VBNewLine _
    & &quot;Days Of Week: &quot; & objJob.DaysOfWeek & VBNewLine _
    & &quot;Description: &quot; & objJob.Description & VBNewLine _
    & &quot;Elapsed Time: &quot; & objJob.ElapsedTime & VBNewLine _
    & &quot;Install Date: &quot; & objJob.InstallDate & VBNewLine _
    & &quot;Interact with Desktop: &quot; & objJob.InteractWithDesktop & VBNewLine _
    & &quot;Job ID: &quot; & objJob.JobId & VBNewLine _
    & &quot;Job Status: &quot; & objJob.JobStatus & VBNewLine _
    & &quot;Name: &quot; & objJob.Name & VBNewLine _
    & &quot;Notify: &quot; & objJob.Notify & VBNewLine _
    & &quot;Owner: &quot; & objJob.Owner & VBNewLine _
    & &quot;Priority: &quot; & objJob.Priority & VBNewLine _
    & &quot;Run Repeatedly: &quot; & objJob.RunRepeatedly & VBNewLine _
    & &quot;Start Time: &quot; & objJob.StartTime & VBNewLine _
    & &quot;Status: &quot; & objJob.Status & VBNewLine _
    & &quot;Time Submitted: &quot; & objJob.TimeSubmitted & VBNewLine _
    & &quot;Until Time: &quot; & objJob.UntilTime
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="fcabf-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fcabf-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcabf-140">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="fcabf-140">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="fcabf-141">WMI C++ Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="fcabf-141">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="fcabf-142">Technet scriptcenter</span><span class="sxs-lookup"><span data-stu-id="fcabf-142">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

