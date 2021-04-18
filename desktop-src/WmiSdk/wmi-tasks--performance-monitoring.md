---
description: Verwenden Sie die WMI-Klassen, die Daten aus Leistungsindikatoren abrufen, um auf Daten über die Computerleistung zuzugreifen und diese zu aktualisieren.
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: 'WMI-Tasks: Leistungsüberwachung'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbb254e14280bec5a928bdc32aaa9a3e03c7a4f4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106361253"
---
# <a name="wmi-tasks-performance-monitoring"></a><span data-ttu-id="bbd3b-103">WMI-Tasks: Leistungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="bbd3b-103">WMI Tasks: Performance Monitoring</span></span>

<span data-ttu-id="bbd3b-104">Verwenden Sie die WMI-Klassen, die Daten aus Leistungsindikatoren abrufen, um auf Daten über die Computerleistung zuzugreifen und diese zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-104">Use the WMI classes that obtain data from performance counters to access and refresh data about computer performance.</span></span> <span data-ttu-id="bbd3b-105">Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bbd3b-105">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span> <span data-ttu-id="bbd3b-106">Weitere Informationen finden Sie unter [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md) und über [Wachen von Leistungsdaten](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="bbd3b-106">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

<span data-ttu-id="bbd3b-107">In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="bbd3b-108">Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="bbd3b-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="bbd3b-109">Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="bbd3b-110">**So führen Sie ein Skript aus**</span><span class="sxs-lookup"><span data-stu-id="bbd3b-110">**To run a script**</span></span>

1.  <span data-ttu-id="bbd3b-111">Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="bbd3b-112">Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="bbd3b-113">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="bbd3b-114">Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="bbd3b-115">Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="bbd3b-116">Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="bbd3b-117">Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="bbd3b-118">Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="bbd3b-119">Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="bbd3b-120">In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbd3b-121">Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="bbd3b-121">How do I...</span></span></th>
<th><span data-ttu-id="bbd3b-122">WMI-Klassen oder-Methoden</span><span class="sxs-lookup"><span data-stu-id="bbd3b-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bbd3b-123">... Abrufen der Leistungsdaten, die im Dienstprogramm "Perfmon" in einem Skript angezeigt werden?</span><span class="sxs-lookup"><span data-stu-id="bbd3b-123">...obtain the performance counter data that I can see in the Perfmon utility in a script?</span></span></td>
<td><span data-ttu-id="bbd3b-124">Verwenden Sie Klassen, deren Namen mit &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a>beginnen &quot; , z. b. <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-124">Use classes that have names that begin with &quot;<a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a>&quot;, for example <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="bbd3b-125">Eigenschaften mit Namen wie <strong>pagefilebytes</strong> entsprechen Leistungsindikatoren, die in Perfmon angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-125">Properties with names like <strong>PageFileBytes</strong> correspond to performance counters you see in Perfmon.</span></span> <span data-ttu-id="bbd3b-126">Die &quot; Win32_PerfFormattedData &quot; Klassen berechnen die Endwerte der Zähler für Sie.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-126">The &quot;Win32_PerfFormattedData&quot; classes calculate the final values of counters for you.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbd3b-127">... erhalten Sie fortlaufende Leistungsdaten für einen einzelnen Prozess, ein Laufwerk und andere Daten?</span><span class="sxs-lookup"><span data-stu-id="bbd3b-127">...get on-going performance data for a single process, disk drive, and other data?</span></span></td>
<td><span data-ttu-id="bbd3b-128">Verwenden Sie die <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> oder die entsprechende formatierte <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Leistungs Leistungs</a> -und <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> Methode.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-128">Use the <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> or the appropriate formatted <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Performance Counter Class</a> and the <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> method.</span></span> <span data-ttu-id="bbd3b-129">Weitere Informationen finden Sie unter <a href="scripting-with-swbemobject.md">Skripterstellung mit "Swap</a>".</span><span class="sxs-lookup"><span data-stu-id="bbd3b-129">For more information, see <a href="scripting-with-swbemobject.md">Scripting with SWbemObject</a>.</span></span><br/> <span data-ttu-id="bbd3b-130">Verwenden Sie in C++ <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>iwbemconfigurerefresher:: addobjectbypath</strong></a> und <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>iwbemrefresh Sher:: Refresh</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-130">In C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher::AddObjectByPath</strong></a> and <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher::Refresh</strong></a>.</span></span> <span data-ttu-id="bbd3b-131">Weitere Informationen finden Sie unter über <a href="monitoring-performance-data.md">Wachen von Leistungsdaten</a>.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-131">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span><br/> <span data-ttu-id="bbd3b-132">Das folgende Skript wird so lange ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-132">The following script runs until the computer is restarted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="bbd3b-133">Um das Skript manuell anzuhalten, verwenden Sie den Task-Manager, um den Prozess zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-133">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="bbd3b-134">Verwenden Sie zum Programm <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>gesteuerten beenden die Beendigungs Methode in</strong></a> der <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> -Klasse.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-134">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbd3b-135">VB</span><span class="sxs-lookup"><span data-stu-id="bbd3b-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set PerfProcess = objWMIService.Get(_
    &quot;Win32_PerfFormattedData_PerfProc_Process.Name=&#39;Idle&#39;&quot;)

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbd3b-136">... erhalten Sie fortlaufende Leistungsdaten für alle Prozesse ohne wiederholtes abrufen?</span><span class="sxs-lookup"><span data-stu-id="bbd3b-136">...get on-going performance data for all processes without repeated polling?</span></span></td>
<td><p><span data-ttu-id="bbd3b-137">Verwenden Sie Klassen, die Namen haben, die mit Win32_PerfFormattedData beginnen, &quot; &quot; und ein <a href="swbemrefresher.md"><strong>Swap</strong></a> -Aktualisierungs-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-137">Use classes that have names that begin with &quot;Win32_PerfFormattedData&quot; and an <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> object.</span></span> <span data-ttu-id="bbd3b-138">Das Aktualisierungs Programm enthält die Objekte, sodass Sie die Auflistung nicht wiederholt erhalten müssen.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-138">The refresher holds the objects so you do not need to get the collection repeatedly.</span></span> <span data-ttu-id="bbd3b-139">Es sind mindestens zwei Werte erforderlich, um Leistungsdaten zu berechnen, da die meisten Leistungsindikatoren Raten Indikatoren sind.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-139">A minimum of two values are needed to calculate performance data because most counters are rate counters.</span></span> <span data-ttu-id="bbd3b-140">Wenn Sie die Aktualisierungsdaten zum ersten Mal anzeigen, ist es leer.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-140">The first time you display the refresher data it is empty.</span></span></p>
<p><span data-ttu-id="bbd3b-141">Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-141">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="bbd3b-142">Um das Skript manuell anzuhalten, verwenden Sie den Task-Manager, um den Prozess zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-142">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="bbd3b-143">Verwenden Sie zum Programm <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>gesteuerten beenden die Beendigungs Methode in</strong></a> der <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> -Klasse.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-143">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbd3b-144">VB</span><span class="sxs-lookup"><span data-stu-id="bbd3b-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set objRefresher = CreateObject(&quot;WbemScripting.Swbemrefresher&quot;)
Set objProcessor = objRefresher.AddEnum _
    (objWMIService, _
    &quot;Win32_PerfFormattedData_PerfOS_Processor&quot;).ObjectSet

While (True)
    objRefresher.Refresh
        For each RefreshItem in objRefresher
            For each objProcess in RefreshItem.ObjectSet
                Wscript.Echo objProcess.GetObjectText_
            Next
        Next
     Wscript.Sleep 5000
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbd3b-145">... erhalten und berechnen Sie Leistungsdaten für Prozesse unter Windows 2000?</span><span class="sxs-lookup"><span data-stu-id="bbd3b-145">...get and calculate performance data for processes on Windows 2000?</span></span></td>
<td><p><span data-ttu-id="bbd3b-146">Verwenden Sie die &quot; Win32_PerfRawData &quot; Klassen, z. b. <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-146">Use the &quot;Win32_PerfRawData&quot; classes, such as <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="bbd3b-147">Die Eigenschaften Daten, z. b. " <strong>prozesprozessortime</strong>", werden für einen bestimmten Prozess zweimal angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-147">Get the property data, such as <strong>PercentProcessorTime</strong>, twice for a specific process.</span></span> <span data-ttu-id="bbd3b-148">Suchen Sie die im <a href="countertype-qualifier.md"><strong>CounterType</strong></a> -Qualifizierer für die Eigenschaft angegebene Formel, und berechnen Sie.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-148">Look up the formula specified in the <a href="countertype-qualifier.md"><strong>CounterType</strong></a> qualifier for the property and calculate.</span></span> <span data-ttu-id="bbd3b-149">Der CounterType im Beispiel ist <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-149">The CounterType in the example is <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span></span> <span data-ttu-id="bbd3b-150">Weitere Informationen finden Sie unter über <a href="monitoring-performance-data.md">Wachen von Leistungsdaten</a>.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-150">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span></p>
<p><span data-ttu-id="bbd3b-151">Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-151">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="bbd3b-152">Um das Skript manuell anzuhalten, verwenden Sie den Task-Manager, um den Prozess zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-152">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="bbd3b-153">Verwenden Sie zum Programm <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>gesteuerten beenden die Beendigungs Methode in</strong></a> der <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> -Klasse.</span><span class="sxs-lookup"><span data-stu-id="bbd3b-153">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bbd3b-154">VB</span><span class="sxs-lookup"><span data-stu-id="bbd3b-154">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)

While (True)
    Set object1 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N1 = object1.PercentProcessorTime
    D1 = object1.TimeStamp_Sys100NS
    Wscript.Sleep(1000)
    set object2 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N2 = object2.PercentProcessorTime
    D2 = object2.TimeStamp_Sys100NS
    &#39; CounterType - PERF_100NSEC_TIMER_INV
    &#39; Formula - (1- ((N2 - N1) / (D2 - D1))) x 100
    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    Wscript.Echo &quot;% Processor Time=&quot; , PercentProcessorTime
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="bbd3b-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbd3b-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbd3b-156">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bbd3b-156">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="bbd3b-157">WMI C++ Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="bbd3b-157">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="bbd3b-158">Technet scriptcenter</span><span class="sxs-lookup"><span data-stu-id="bbd3b-158">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
