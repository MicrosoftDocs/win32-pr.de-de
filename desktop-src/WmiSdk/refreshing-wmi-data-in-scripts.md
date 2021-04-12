---
description: In Überwachungs Skripts können Sie nachfolgende Aufrufe von GetObject vermeiden, indem Sie ein "Swap-Aktualisierungs"-Objekt verwenden. Das taubemaktualisierungs-Objekt ist ein Container, der mehrere WMI-Objekte enthalten kann, deren Daten mit einem einzigen-Befehl aktualisiert werden können.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Aktualisieren von WMI-Daten in Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0f17ce718fcf5b57e4f3204337634af4129d24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216894"
---
# <a name="refreshing-wmi-data-in-scripts"></a><span data-ttu-id="b94bd-104">Aktualisieren von WMI-Daten in Skripts</span><span class="sxs-lookup"><span data-stu-id="b94bd-104">Refreshing WMI Data in Scripts</span></span>

<span data-ttu-id="b94bd-105">In Überwachungs Skripts können Sie nachfolgende Aufrufe von **GetObject** vermeiden, indem Sie ein " [**Swap**](swbemrefresher.md) -Aktualisierungs"-Objekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="b94bd-105">In monitoring scripts, you can avoid successive calls to **GetObject** by using an [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="b94bd-106">Das **taubemaktualisierungs** -Objekt ist ein Container, der mehrere WMI-Objekte enthalten kann, deren Daten mit einem einzigen-Befehl aktualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="b94bd-106">The **SWbemRefresher** object is a container that can hold several WMI objects whose data can be refreshed in one call.</span></span>

<span data-ttu-id="b94bd-107">Zum Abrufen präziser Daten von WMI-Leistungsklassen, wie z. b. [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) oder anderer vorinstallierter, von [**Win32 \_ perf**](/windows/desktop/CIMWin32Prov/win32-perf)abgeleiteter Klassen, ist das Verwenden eines " [**Swap**](swbemrefresher.md) "-Objekts erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b94bd-107">Using an [**SWbemRefresher**](swbemrefresher.md) object is required to get accurate data from WMI performance classes, such as [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) or other preinstalled classes derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span>

<span data-ttu-id="b94bd-108">Im folgenden Verfahren wird beschrieben, wie Daten in-Skripts aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b94bd-108">The following procedure describes how to refresh data in scripts.</span></span>

<span data-ttu-id="b94bd-109">**So aktualisieren Sie Daten in Skripts**</span><span class="sxs-lookup"><span data-stu-id="b94bd-109">**To refresh data in scripts**</span></span>

1.  <span data-ttu-id="b94bd-110">Rufen Sie " **kreateobject** " auf, um ein Metadatenobjekt für " [**Swap**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="b94bd-110">Call **CreateObject** to create an [**SWbemRefresher**](swbemrefresher.md) refresher object.</span></span>

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  <span data-ttu-id="b94bd-111">Stellen Sie eine Verbindung zum WMI-Namespace her.</span><span class="sxs-lookup"><span data-stu-id="b94bd-111">Connect to the WMI namespace.</span></span> <span data-ttu-id="b94bd-112">Stellen Sie eine Verbindung mit **root \\ CIMV2** her, um vorinstallierte [**Win32 \_ perf**](/windows/desktop/CIMWin32Prov/win32-perf) -Leistungsklassen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b94bd-112">To use preinstalled [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) performances classes, connect to **root\\cimv2**.</span></span>

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  <span data-ttu-id="b94bd-113">Fügen Sie ein einzelnes-Objekt (Aufrufen von " [**slibemaktualisierungs-. Add**](swbemrefresher-add.md)") oder eine Auflistung (Aufrufen von " [**slibemaktualisierungs. AddEnum**](swbemrefresher-addenum.md)") zum Aktualisierungs Programm hinzu.</span><span class="sxs-lookup"><span data-stu-id="b94bd-113">Add a single object (call [**SWbemRefresher.Add**](swbemrefresher-add.md)) or a collection (call [**SWbemRefresher.AddEnum**](swbemrefresher-addenum.md)) to the refresher.</span></span>

    <span data-ttu-id="b94bd-114">Verwenden Sie die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleiteten vorab berechneten Daten Klassen, z. b. [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) anstelle von [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="b94bd-114">Use the precalculated data classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), for example, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) instead of [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="b94bd-115">Andernfalls müssen Sie die Werte für alle Eigenschaften berechnen, die keine einfachen Leistungsindikatoren sind.</span><span class="sxs-lookup"><span data-stu-id="b94bd-115">Otherwise, you must calculate the values for all of the properties other than simple counters.</span></span>

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  <span data-ttu-id="b94bd-116">Aktualisieren Sie die Daten einmal, um die anfänglichen Leistungsdaten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b94bd-116">Refresh the data one time to get the initial performance data.</span></span>

    <span data-ttu-id="b94bd-117">Rufen Sie entweder die Methode " [**errbemrefresh Sher. Refresh**](swbemrefresher-refresh.md) " oder die generische Methode " [**errbemubjectex. Refresh \_**](swbemobjectex-refresh-.md) " auf.</span><span class="sxs-lookup"><span data-stu-id="b94bd-117">Call either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the generic [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

    ```VB
    objRefresher.Refresh
    ```

    

5.  <span data-ttu-id="b94bd-118">Wenn Sie die Leistung überwachen und eine Sammlung im Aktualisierungs Objekt enthalten, durchlaufen Sie die Auflistungs Objekte.</span><span class="sxs-lookup"><span data-stu-id="b94bd-118">If you are monitoring performance and have a collection in the refresher object, loop through the collection objects.</span></span>

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  <span data-ttu-id="b94bd-119">Löschen Sie die Elemente aus dem Aktualisierungs Programm, indem Sie die Option " [**Swap. DeleteAll**](swbemrefresher-deleteall.md) " aufrufen oder bestimmte Elemente entfernen, indem Sie " [**Swap. Remove**](swbemrefresher-remove.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b94bd-119">Clear the items from the refresher by calling [**SWbemRefresher.DeleteAll**](swbemrefresher-deleteall.md) or remove specific items by calling [**SwbemRefresher.Remove**](swbemrefresher-remove.md).</span></span>

<span data-ttu-id="b94bd-120">Im folgenden VBScript-Codebeispiel wird gezeigt, wie ein einzelnes Objekt auf dem lokalen Computer aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b94bd-120">The following VBScript code example shows how to refresh a single object on the local computer.</span></span> <span data-ttu-id="b94bd-121">Das Skript erstellt einen Aktualisierungs Container und fügt eine Instanz eines Enumerators für [**Win32 \_ perfformatteddata \_ perfproc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) -Instanzen hinzu.</span><span class="sxs-lookup"><span data-stu-id="b94bd-121">The script creates a refresher container and adds an instance of an enumerator for [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instances.</span></span> <span data-ttu-id="b94bd-122">Der [**Aktualisierungs**](swbemrefresher-refresh.md) Aufruf wird dreimal durchgeführt, um die Änderungen in der Eigenschaft " **prozentuprocessortime** " für Prozesse zu veranschaulichen, die mehr als einen Prozentsatz der Prozessorzeit verwenden.</span><span class="sxs-lookup"><span data-stu-id="b94bd-122">The [**Refresh**](swbemrefresher-refresh.md) call is made three times to demonstrate the changes in the **PercentProcessorTime** property for processes using more than one percent of the processor time.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
Set objServicesCimv2 = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
If Err = 0 Then 
Set objRefreshableItem = _
    objRefresher.AddEnum(objServicesCimv2 ,"Win32_PerfFormattedData_PerfProc_Process")
objRefresher.Refresh
' Loop through the processes three times to locate  
'    and display all the process currently using 
'    more than 1 % of the process time. Refresh on each pass.
For i = 1 to 3
    Wscript.Echo "Refresh number " & i 
    objRefresher.Refresh 
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine & Process.PercentProcessorTime & "%"
        End If
    Next
Next
Else
    WScript.Echo Err.Description
End If
```



<span data-ttu-id="b94bd-123">Die [**Index**](swbemrefreshableitem-index.md) -Eigenschaft des zurückgegebenen " [**taubemfreshableitem**](swbemrefreshableitem.md) "-Objekts stellt den Index des-Objekts in der Aktualisierungs-Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="b94bd-123">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span> <span data-ttu-id="b94bd-124">Sie können die Eigenschaft ' [**Swap. isset**](swbemrefreshableitem-isset.md) ' der Eigenschaft ' Swap ' aufzurufen, um zu bestimmen, ob ein Element in einem Aktualisierungs Programm ein einzelnes Element oder eine Auflistung ist.</span><span class="sxs-lookup"><span data-stu-id="b94bd-124">You can call [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) property to determine whether or not an item in a refresher is a single item or a collection.</span></span> <span data-ttu-id="b94bd-125">Wenn Sie auf ein einzelnes Element zugreifen möchten, verwenden Sie die Eigenschaft " [**Swap. Object**](swbemrefreshableitem-object.md) ".</span><span class="sxs-lookup"><span data-stu-id="b94bd-125">To access a single item, use the [**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) property.</span></span> <span data-ttu-id="b94bd-126">Wenn Sie den Aufrufvorgang für " **Swap. Object**" nicht durchführen, schlägt das Skript fehl, wenn Sie versuchen, auf das Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b94bd-126">If you do not make the call to **SWbemRefreshableItem.Object**, then the script fails when you try to access the object.</span></span> <span data-ttu-id="b94bd-127">Um auf eine Auflistung zuzugreifen, verwenden Sie die Eigenschaft " [**Swap. ObjectSet**](swbemrefreshableitem-objectset.md) ".</span><span class="sxs-lookup"><span data-stu-id="b94bd-127">To access a collection, use the [**SWbemRefreshableItem.ObjectSet**](swbemrefreshableitem-objectset.md) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b94bd-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b94bd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b94bd-129">Leistungs Leistungsdaten-Klassen</span><span class="sxs-lookup"><span data-stu-id="b94bd-129">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="b94bd-130">Zugreifen auf Leistungsdaten im Skript</span><span class="sxs-lookup"><span data-stu-id="b94bd-130">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="b94bd-131">WMI-Tasks: Leistungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="b94bd-131">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="b94bd-132">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="b94bd-132">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
