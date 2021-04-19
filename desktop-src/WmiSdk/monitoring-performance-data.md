---
description: Mithilfe von WMI können Sie Programm gesteuert auf System Leistungsdaten von Objekten in den Leistungs Bibliotheken zugreifen.
ms.assetid: a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d
ms.tgt_platform: multiple
title: Überwachen von Leistungsdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95cee18ba88a8aff920c2d14b5709a0fd913e2ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364239"
---
# <a name="monitoring-performance-data"></a><span data-ttu-id="497e8-103">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="497e8-103">Monitoring Performance Data</span></span>

<span data-ttu-id="497e8-104">Mithilfe von WMI können Sie Programm gesteuert auf System Leistungsdaten von Objekten in den Leistungs Bibliotheken zugreifen.</span><span class="sxs-lookup"><span data-stu-id="497e8-104">Using WMI, you can access system counter data programmatically from objects in the performance libraries.</span></span> <span data-ttu-id="497e8-105">Dies sind die gleichen Leistungsdaten, die im System Monitor im Dienstprogramm Perfmon angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="497e8-105">This is the same performance data that appears in the System Monitor in the Perfmon utility.</span></span> <span data-ttu-id="497e8-106">Verwenden Sie die vorinstallierten [Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes) Daten-Klassen, um Leistungsdaten in Skripts oder C++-Anwendungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="497e8-106">Use the preinstalled [performance counter classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) to obtain performance data in scripts or C++ applications.</span></span>

<span data-ttu-id="497e8-107">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="497e8-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="497e8-108">WMI-Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="497e8-108">WMI Performance Classes</span></span>](#wmi-performance-classes)
-   [<span data-ttu-id="497e8-109">Leistungsdaten Anbieter</span><span class="sxs-lookup"><span data-stu-id="497e8-109">Performance Data Providers</span></span>](#performance-data-providers)
-   [<span data-ttu-id="497e8-110">Verwenden von formatierten Leistungsdaten Klassen</span><span class="sxs-lookup"><span data-stu-id="497e8-110">Using Formatted Performance Data Classes</span></span>](#using-formatted-performance-data-classes)
-   [<span data-ttu-id="497e8-111">Verwenden von rohleistungs Daten-Klassen</span><span class="sxs-lookup"><span data-stu-id="497e8-111">Using Raw Performance Data Classes</span></span>](#using-raw-performance-data-classes)
-   [<span data-ttu-id="497e8-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="497e8-112">Related topics</span></span>](#related-topics)

## <a name="wmi-performance-classes"></a><span data-ttu-id="497e8-113">WMI-Leistungsklassen</span><span class="sxs-lookup"><span data-stu-id="497e8-113">WMI Performance Classes</span></span>

<span data-ttu-id="497e8-114">Beispielsweise wird das "Network Interface"-Objekt im System Monitor in WMI durch die [**Win32 \_ perfrawdata \_ tcpip \_ NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) -Klasse für Rohdaten und die [**Win32 \_ perfformatteddata \_ tcpip \_ NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) -Klasse für vorab berechnete oder formatierte Daten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="497e8-114">As an example, the "NetworkInterface" object, in System Monitor, is represented in WMI by the [**Win32\_PerfRawData\_Tcpip\_NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) class for raw data and the [**Win32\_PerfFormattedData\_Tcpip\_NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class for precalculated, or formatted data.</span></span> <span data-ttu-id="497e8-115">Klassen, die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitet werden, müssen mit [*einem Aktualisierungs*](gloss-r.md) Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="497e8-115">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) must be used with a [*refresher*](gloss-r.md) object.</span></span> <span data-ttu-id="497e8-116">Bei Rohdaten Klassen muss die C++-Anwendung oder das Skript Berechnungen ausführen, um dieselbe Ausgabe wie Perfmon.exe zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="497e8-116">On raw data classes, your C++ application or script must perform calculations to obtain the same output as Perfmon.exe.</span></span> <span data-ttu-id="497e8-117">Formatierte Daten Klassen stellen vorab berechnete Daten bereit.</span><span class="sxs-lookup"><span data-stu-id="497e8-117">Formatted data classes supply precalculated data.</span></span> <span data-ttu-id="497e8-118">Weitere Informationen zum Abrufen von Daten in C++-Anwendungen finden Sie unter [zugreifen auf Leistungsdaten in C++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="497e8-118">For more information about obtaining data in C++ applications, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="497e8-119">Informationen zur Skripterstellung finden Sie unter [zugreifen auf Leistungsdaten im Skript](accessing-performance-data-in-script.md) und Aktualisieren von [WMI-Daten in](refreshing-wmi-data-in-scripts.md)Skripts.</span><span class="sxs-lookup"><span data-stu-id="497e8-119">For scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="497e8-120">Im folgenden VBScript-Codebeispiel wird der [**Win32 \_ perfformatteddata \_ perfproc- \_ Prozess**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) verwendet, um Leistungsdaten für den Leerlauf Prozess zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="497e8-120">The following VBScript code example uses [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) to obtain performance data for the Idle process.</span></span> <span data-ttu-id="497e8-121">Das Skript zeigt die gleichen Daten an, die in Perfmon für den Leistungs Monitor "Prozessorzeit (%)" des Prozess Objekts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="497e8-121">The script displays the same data that appears in Perfmon for the % Processor Time counter of the Process object.</span></span> <span data-ttu-id="497e8-122">Der Aktualisierungs Vorgang wird durch den Aufrufen von " [**errbemubjectex. Refresh \_**](swbemobjectex-refresh-.md) " durchführt.</span><span class="sxs-lookup"><span data-stu-id="497e8-122">The call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) performs the refresh operation.</span></span> <span data-ttu-id="497e8-123">Beachten Sie, dass die Daten bei der Lease einmal aktualisiert werden müssen, um eine Baseline zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="497e8-123">Be aware that the data must be refreshed, at lease once, to obtain a baseline.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")
set PerfProcess = objWMIService.Get(_
    "Win32_PerfFormattedData_PerfProc_Process.Name='Idle'")

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend
```



<span data-ttu-id="497e8-124">Leistungs Leistungsdaten-Klassen können auch statistische Daten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="497e8-124">Performance counter classes can also provide statistical data.</span></span> <span data-ttu-id="497e8-125">Weitere Informationen finden Sie unter Abrufen [statistischer Leistungsdaten](obtaining-statistical-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="497e8-125">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="performance-data-providers"></a><span data-ttu-id="497e8-126">Leistungsdaten Anbieter</span><span class="sxs-lookup"><span data-stu-id="497e8-126">Performance Data Providers</span></span>

<span data-ttu-id="497e8-127">WMI verfügt über vorinstallierte Anbieter, die die Systemleistung sowohl auf dem lokalen System als auch remote überwachen.</span><span class="sxs-lookup"><span data-stu-id="497e8-127">WMI has preinstalled providers that monitor system performance on both the local system and remotely.</span></span> <span data-ttu-id="497e8-128">Der [wmiperfclass](wmiperfclass-provider.md) -Anbieter erstellt die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) abgeleiteten Klassen und aus [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="497e8-128">The [WmiPerfClass](wmiperfclass-provider.md) provider creates the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="497e8-129">Der [wmiperfinst](wmiperfinst-provider.md) -Anbieter liefert Daten dynamisch für rohklassen und formatierte Klassen.</span><span class="sxs-lookup"><span data-stu-id="497e8-129">The [WmiPerfInst](wmiperfinst-provider.md) provider supplies data dynamically to both raw and formatted classes.</span></span>

## <a name="using-formatted-performance-data-classes"></a><span data-ttu-id="497e8-130">Verwenden von formatierten Leistungsdaten Klassen</span><span class="sxs-lookup"><span data-stu-id="497e8-130">Using Formatted Performance Data Classes</span></span>

<span data-ttu-id="497e8-131">Im folgenden VBScript-Codebeispiel werden Leistungsdaten zu Arbeitsspeicher, Datenträger Partitionen und Server Arbeits Warteschlangen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="497e8-131">The following VBScript code example obtains performance data about memory, disk partitions, and server work queues.</span></span> <span data-ttu-id="497e8-132">Das Skript bestimmt dann, ob die Werte in einem akzeptablen Bereich liegen.</span><span class="sxs-lookup"><span data-stu-id="497e8-132">The script then determines if the values are within an acceptable range.</span></span>

<span data-ttu-id="497e8-133">Das Skript verwendet die folgenden WMI-Anbieter Objekte und Skript Objekte:</span><span class="sxs-lookup"><span data-stu-id="497e8-133">The script uses the following WMI provider objects and scripting objects:</span></span>

-   <span data-ttu-id="497e8-134">Vorinstallierte WMI-Leistungs Leistungsdaten-Klassen.</span><span class="sxs-lookup"><span data-stu-id="497e8-134">Preinstalled WMI performance counter classes.</span></span>
-   <span data-ttu-id="497e8-135">Das aktualisierbare Objekt, [**Swap**](swbemrefresher.md)-Aktualisierungs Programm.</span><span class="sxs-lookup"><span data-stu-id="497e8-135">The refresher object, [**SWbemRefresher**](swbemrefresher.md).</span></span>
-   <span data-ttu-id="497e8-136">Elemente, die dem Aktualisierungs Container hinzugefügt werden sollen, " [ **Swap freshableitem** "](swbemrefreshableitem.md)</span><span class="sxs-lookup"><span data-stu-id="497e8-136">Items to add to the refresher container, [**SWbemRefreshableItem**](swbemrefreshableitem.md)</span></span>


```VB
Set objCimv2 = GetObject("winmgmts:root\cimv2")
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add items to the SWbemRefresher
' Without the SWbemRefreshableItem.ObjectSet call,
' the script will fail
Set objMemory = objRefresher.AddEnum _
    (objCimv2, _ 
    "Win32_PerfFormattedData_PerfOS_Memory").ObjectSet
Set objDiskQueue = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfDisk_LogicalDisk").ObjectSet
Set objQueueLength = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfNet_ServerWorkQueues").ObjectSet

' Initial refresh needed to get baseline values
objRefresher.Refresh
intTotalHealth = 0
' Do three refreshes to get data
For i = 1 to 3
    WScript.Echo "Refresh " & i
    For each intAvailableBytes in objMemory
        WScript.Echo "Available megabytes of memory: " _
            & intAvailableBytes.AvailableMBytes
        If intAvailableBytes.AvailableMBytes < 4 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intDiskQueue in objDiskQueue
        WScript.Echo "Current disk queue length " & "Name: " _
            & intDiskQueue.Name & ":" _
            & intDiskQueue.CurrentDiskQueueLength
        If intDiskQueue.CurrentDiskQueueLength > 2 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intServerQueueLength in objQueueLength
        WScript.Echo "Server work queue length: " _
            & intServerQueueLength.QueueLength
        If intServerQueueLength.QueueLength > 4 Then
            intTotalHealth = intTotalHealth + 1                       
        End If
    Wscript.Echo "  "
    Next
    If intTotalHealth > 0 Then
        Wscript.Echo "Unhealthy."
    Else
        Wscript.Echo "Healthy."
    End If
    intTotalHealth = 0
    Wscript.Sleep 5000
' Refresh data for all objects in the collection
    objRefresher.Refresh
Next
```



## <a name="using-raw-performance-data-classes"></a><span data-ttu-id="497e8-137">Verwenden von rohleistungs Daten-Klassen</span><span class="sxs-lookup"><span data-stu-id="497e8-137">Using Raw Performance Data Classes</span></span>

<span data-ttu-id="497e8-138">Im folgenden VBScript-Codebeispiel wird die Rohdaten Prozessorzeit (aktuell%) auf dem lokalen Computer abgerufen und in einen Prozentsatz konvertiert.</span><span class="sxs-lookup"><span data-stu-id="497e8-138">The following VBScript code example obtains raw, current percent processor time on the local computer and converts it to a percentage.</span></span> <span data-ttu-id="497e8-139">Das Beispiel zeigt, wie Sie rohleistungs Daten aus der Eigenschaft " **%processortime** " der [**Win32 \_ perfrawdata \_ perfos- \_ Prozessor**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) Klasse abrufen.</span><span class="sxs-lookup"><span data-stu-id="497e8-139">The example shows you how to obtain raw performance data from the **PercentProcessorTime** property of the [**Win32\_PerfRawData\_PerfOS\_Processor**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class.</span></span>

<span data-ttu-id="497e8-140">Um den Wert für die Prozessorzeit in Prozent zu berechnen, müssen Sie die Formel suchen.</span><span class="sxs-lookup"><span data-stu-id="497e8-140">To calculate the percent processor time value, you must locate the formula.</span></span> <span data-ttu-id="497e8-141">Suchen Sie den Wert im **CounterType** -Qualifizierer für die Eigenschaft " **prozentuprocessortime** " in der Tabelle " [**CounterType Qualifizierer**](countertype-qualifier.md) ", um den konstanten Namen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="497e8-141">Look up the value in the **CounterType** qualifier for the **PercentProcessorTime** property in the [**CounterType Qualifier**](countertype-qualifier.md) table to get the constant name.</span></span> <span data-ttu-id="497e8-142">Suchen Sie den konstanten Namen in den [Counter-Typen](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) , um die Formel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="497e8-142">Locate the constant name in [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) to obtain the formula.</span></span>


```VB
Set objService = GetObject( _
    "Winmgmts:{impersonationlevel=impersonate}!\Root\Cimv2")

For i = 1 to 8
    Set objInstance1 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N1 = objInstance1.PercentProcessorTime
    D1 = objInstance1.TimeStamp_Sys100NS

'Sleep for two seconds = 2000 ms
    WScript.Sleep(2000)

    Set perf_instance2 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N2 = perf_instance2.PercentProcessorTime
    D2 = perf_instance2.TimeStamp_Sys100NS
' Look up the CounterType qualifier for the PercentProcessorTime 
' and obtain the formula to calculate the meaningful data. 
' CounterType - PERF_100NSEC_TIMER_INV
' Formula - (1- ((N2 - N1) / (D2 - D1))) x 100

    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    WScript.Echo "% Processor Time=" , Round(PercentProcessorTime,2)
Next
```



## <a name="related-topics"></a><span data-ttu-id="497e8-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="497e8-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="497e8-144">Verwenden von WMI</span><span class="sxs-lookup"><span data-stu-id="497e8-144">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
