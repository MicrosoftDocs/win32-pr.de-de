---
description: Mithilfe von WMI können Sie programmgesteuert über Objekte in den Leistungsbibliotheken auf Systemzählerdaten zugreifen.
ms.assetid: a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d
ms.tgt_platform: multiple
title: Überwachen von Leistungsdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4f3ddd5024fb27d83f08225fa65faaa2e7d02cdd28189c86fc979175861453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317104"
---
# <a name="monitoring-performance-data"></a>Überwachen von Leistungsdaten

Mithilfe von WMI können Sie programmgesteuert über Objekte in den Leistungsbibliotheken auf Systemzählerdaten zugreifen. Dies sind die gleichen Leistungsdaten, die im Systemmonitor des Hilfsprogramms Perfmon angezeigt werden. Verwenden Sie die vorinstallierten [Leistungsindikatorklassen,](/windows/desktop/CIMWin32Prov/performance-counter-classes) um Leistungsdaten in Skripts oder C++-Anwendungen abzurufen.

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [WMI-Leistungsklassen](#wmi-performance-classes)
-   [Leistungsdatenanbieter](#performance-data-providers)
-   [Verwenden formatierter Leistungsdatenklassen](#using-formatted-performance-data-classes)
-   [Verwenden von Unformatierten Leistungsdatenklassen](#using-raw-performance-data-classes)
-   [Zugehörige Themen](#related-topics)

## <a name="wmi-performance-classes"></a>WMI-Leistungsklassen

Als Beispiel wird das Objekt "NetworkInterface" im Systemmonitor in WMI durch die [**Win32 \_ PerfRawData \_ Tcpip \_ NetworkInterface-Klasse**](./retrieving-raw-and-formatted-performance-data.md) für Rohdaten und die [**Win32 \_ PerfFormattedData \_ Tcpip \_ NetworkInterface-Klasse**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) für vorab berechnete oder formatierte Daten dargestellt. Von [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) abgeleitete Klassen müssen mit einem [*Aktualisierungsobjekt*](gloss-r.md) verwendet werden. Bei Rohdatenklassen muss Die C++-Anwendung oder das C++-Skript Berechnungen ausführen, um die gleiche Ausgabe wie Perfmon.exe zu erhalten. Formatierte Datenklassen stellen vorab berechnete Daten zur Verfügung. Weitere Informationen zum Abrufen von Daten in C++-Anwendungen finden Sie unter [Zugreifen auf Leistungsdaten in C++.](accessing-performance-data-in-c--.md) Informationen zur Skripterstellung finden Sie unter [Zugreifen auf Leistungsdaten in Skripts](accessing-performance-data-in-script.md) und [Aktualisieren von WMI-Daten in Skripts.](refreshing-wmi-data-in-scripts.md)

Im folgenden VBScript-Codebeispiel wird [**der Win32 \_ PerfFormattedData \_ PerfProc-Prozess \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) verwendet, um Leistungsdaten für den Idle-Prozess abzurufen. Das Skript zeigt die gleichen Daten an, die in Perfmon für den Prozessorzeitindikator %des Process-Objekts angezeigt werden. Der Aufruf von [**SWbemObjectEx.Refresh \_**](swbemobjectex-refresh-.md) führt den Aktualisierungsvorgang aus. Beachten Sie, dass die Daten bei einer Lease einmal aktualisiert werden müssen, um eine Baseline zu erhalten.


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



Leistungsindikatorklassen können auch statistische Daten bereitstellen. Weitere Informationen finden Sie unter [Abrufen statistischer Leistungsdaten.](obtaining-statistical-performance-data.md)

## <a name="performance-data-providers"></a>Leistungsdatenanbieter

WMI verfügt über vorinstallierte Anbieter, die die Systemleistung sowohl auf dem lokalen System als auch remote überwachen. Der [WmiPerfClass-Anbieter](wmiperfclass-provider.md) erstellt die von [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) und [**win32 \_ PerfFormattedData abgeleiteten**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)Klassen. Der [WmiPerfInst-Anbieter](wmiperfinst-provider.md) stellt Daten dynamisch sowohl für unformatierte als auch für formatierte Klassen bereit.

## <a name="using-formatted-performance-data-classes"></a>Verwenden formatierter Leistungsdatenklassen

Das folgende VBScript-Codebeispiel ruft Leistungsdaten zu Arbeitsspeicher, Datenträgerpartitionen und Serverarbeitswarteschlangen ab. Das Skript bestimmt dann, ob die Werte innerhalb eines akzeptablen Bereichs liegen.

Das Skript verwendet die folgenden WMI-Anbieterobjekte und Skriptobjekte:

-   Vorinstallierte WMI-Leistungsindikatorklassen.
-   Das Aktualisierungsobjekt, [**SWbemRefresher.**](swbemrefresher.md)
-   Elemente, die dem Aktualisierungscontainer hinzugefügt werden sollen, [ **SWbemRefreshableItem**](swbemrefreshableitem.md)


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



## <a name="using-raw-performance-data-classes"></a>Verwenden von Unformatierten Leistungsdatenklassen

Im folgenden VBScript-Codebeispiel wird die aktuelle Prozessorzeit in Rohdaten in Prozent auf dem lokalen Computer erhalten und in einen Prozentsatz konvertiert. Das Beispiel zeigt, wie Sie Rohleistungsdaten aus der **PercentProcessorTime-Eigenschaft** der [**Win32 \_ PerfRawData \_ PerfOS-Prozessorklasse \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) abrufen.

Um den Prozessorzeitwert in Prozent zu berechnen, müssen Sie die Formel suchen. Suchen Sie den Wert im **CounterType-Qualifizierer** für die **PercentProcessorTime-Eigenschaft** in der [**CounterType-Qualifizierertabelle,**](countertype-qualifier.md) um den konstanten Namen abzurufen. Suchen Sie den konstanten Namen in [Indikatortypen,](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) um die Formel abzurufen.


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

 

 
