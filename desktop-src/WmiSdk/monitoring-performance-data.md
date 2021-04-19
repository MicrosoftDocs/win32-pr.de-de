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
# <a name="monitoring-performance-data"></a>Überwachen von Leistungsdaten

Mithilfe von WMI können Sie Programm gesteuert auf System Leistungsdaten von Objekten in den Leistungs Bibliotheken zugreifen. Dies sind die gleichen Leistungsdaten, die im System Monitor im Dienstprogramm Perfmon angezeigt werden. Verwenden Sie die vorinstallierten [Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes) Daten-Klassen, um Leistungsdaten in Skripts oder C++-Anwendungen abzurufen.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [WMI-Leistungsklassen](#wmi-performance-classes)
-   [Leistungsdaten Anbieter](#performance-data-providers)
-   [Verwenden von formatierten Leistungsdaten Klassen](#using-formatted-performance-data-classes)
-   [Verwenden von rohleistungs Daten-Klassen](#using-raw-performance-data-classes)
-   [Zugehörige Themen](#related-topics)

## <a name="wmi-performance-classes"></a>WMI-Leistungsklassen

Beispielsweise wird das "Network Interface"-Objekt im System Monitor in WMI durch die [**Win32 \_ perfrawdata \_ tcpip \_ NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) -Klasse für Rohdaten und die [**Win32 \_ perfformatteddata \_ tcpip \_ NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) -Klasse für vorab berechnete oder formatierte Daten dargestellt. Klassen, die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitet werden, müssen mit [*einem Aktualisierungs*](gloss-r.md) Objekt verwendet werden. Bei Rohdaten Klassen muss die C++-Anwendung oder das Skript Berechnungen ausführen, um dieselbe Ausgabe wie Perfmon.exe zu erhalten. Formatierte Daten Klassen stellen vorab berechnete Daten bereit. Weitere Informationen zum Abrufen von Daten in C++-Anwendungen finden Sie unter [zugreifen auf Leistungsdaten in C++](accessing-performance-data-in-c--.md). Informationen zur Skripterstellung finden Sie unter [zugreifen auf Leistungsdaten im Skript](accessing-performance-data-in-script.md) und Aktualisieren von [WMI-Daten in](refreshing-wmi-data-in-scripts.md)Skripts.

Im folgenden VBScript-Codebeispiel wird der [**Win32 \_ perfformatteddata \_ perfproc- \_ Prozess**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) verwendet, um Leistungsdaten für den Leerlauf Prozess zu erhalten. Das Skript zeigt die gleichen Daten an, die in Perfmon für den Leistungs Monitor "Prozessorzeit (%)" des Prozess Objekts angezeigt werden. Der Aktualisierungs Vorgang wird durch den Aufrufen von " [**errbemubjectex. Refresh \_**](swbemobjectex-refresh-.md) " durchführt. Beachten Sie, dass die Daten bei der Lease einmal aktualisiert werden müssen, um eine Baseline zu erhalten.


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



Leistungs Leistungsdaten-Klassen können auch statistische Daten bereitstellen. Weitere Informationen finden Sie unter Abrufen [statistischer Leistungsdaten](obtaining-statistical-performance-data.md).

## <a name="performance-data-providers"></a>Leistungsdaten Anbieter

WMI verfügt über vorinstallierte Anbieter, die die Systemleistung sowohl auf dem lokalen System als auch remote überwachen. Der [wmiperfclass](wmiperfclass-provider.md) -Anbieter erstellt die von [**Win32 \_ perfrawdata**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) abgeleiteten Klassen und aus [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). Der [wmiperfinst](wmiperfinst-provider.md) -Anbieter liefert Daten dynamisch für rohklassen und formatierte Klassen.

## <a name="using-formatted-performance-data-classes"></a>Verwenden von formatierten Leistungsdaten Klassen

Im folgenden VBScript-Codebeispiel werden Leistungsdaten zu Arbeitsspeicher, Datenträger Partitionen und Server Arbeits Warteschlangen abgerufen. Das Skript bestimmt dann, ob die Werte in einem akzeptablen Bereich liegen.

Das Skript verwendet die folgenden WMI-Anbieter Objekte und Skript Objekte:

-   Vorinstallierte WMI-Leistungs Leistungsdaten-Klassen.
-   Das aktualisierbare Objekt, [**Swap**](swbemrefresher.md)-Aktualisierungs Programm.
-   Elemente, die dem Aktualisierungs Container hinzugefügt werden sollen, " [ **Swap freshableitem** "](swbemrefreshableitem.md)


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



## <a name="using-raw-performance-data-classes"></a>Verwenden von rohleistungs Daten-Klassen

Im folgenden VBScript-Codebeispiel wird die Rohdaten Prozessorzeit (aktuell%) auf dem lokalen Computer abgerufen und in einen Prozentsatz konvertiert. Das Beispiel zeigt, wie Sie rohleistungs Daten aus der Eigenschaft " **%processortime** " der [**Win32 \_ perfrawdata \_ perfos- \_ Prozessor**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) Klasse abrufen.

Um den Wert für die Prozessorzeit in Prozent zu berechnen, müssen Sie die Formel suchen. Suchen Sie den Wert im **CounterType** -Qualifizierer für die Eigenschaft " **prozentuprocessortime** " in der Tabelle " [**CounterType Qualifizierer**](countertype-qualifier.md) ", um den konstanten Namen zu erhalten. Suchen Sie den konstanten Namen in den [Counter-Typen](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) , um die Formel zu erhalten.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> </dl>

 

 
