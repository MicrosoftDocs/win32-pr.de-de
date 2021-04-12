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
# <a name="refreshing-wmi-data-in-scripts"></a>Aktualisieren von WMI-Daten in Skripts

In Überwachungs Skripts können Sie nachfolgende Aufrufe von **GetObject** vermeiden, indem Sie ein " [**Swap**](swbemrefresher.md) -Aktualisierungs"-Objekt verwenden. Das **taubemaktualisierungs** -Objekt ist ein Container, der mehrere WMI-Objekte enthalten kann, deren Daten mit einem einzigen-Befehl aktualisiert werden können.

Zum Abrufen präziser Daten von WMI-Leistungsklassen, wie z. b. [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) oder anderer vorinstallierter, von [**Win32 \_ perf**](/windows/desktop/CIMWin32Prov/win32-perf)abgeleiteter Klassen, ist das Verwenden eines " [**Swap**](swbemrefresher.md) "-Objekts erforderlich.

Im folgenden Verfahren wird beschrieben, wie Daten in-Skripts aktualisiert werden.

**So aktualisieren Sie Daten in Skripts**

1.  Rufen Sie " **kreateobject** " auf, um ein Metadatenobjekt für " [**Swap**](swbemrefresher.md) .

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  Stellen Sie eine Verbindung zum WMI-Namespace her. Stellen Sie eine Verbindung mit **root \\ CIMV2** her, um vorinstallierte [**Win32 \_ perf**](/windows/desktop/CIMWin32Prov/win32-perf) -Leistungsklassen zu verwenden.

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  Fügen Sie ein einzelnes-Objekt (Aufrufen von " [**slibemaktualisierungs-. Add**](swbemrefresher-add.md)") oder eine Auflistung (Aufrufen von " [**slibemaktualisierungs. AddEnum**](swbemrefresher-addenum.md)") zum Aktualisierungs Programm hinzu.

    Verwenden Sie die von [**Win32 \_ perfformatteddata**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleiteten vorab berechneten Daten Klassen, z. b. [**Win32 \_ perfformatteddata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) anstelle von [**Win32 \_ perfrawdata \_ perfdisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md). Andernfalls müssen Sie die Werte für alle Eigenschaften berechnen, die keine einfachen Leistungsindikatoren sind.

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  Aktualisieren Sie die Daten einmal, um die anfänglichen Leistungsdaten zu erhalten.

    Rufen Sie entweder die Methode " [**errbemrefresh Sher. Refresh**](swbemrefresher-refresh.md) " oder die generische Methode " [**errbemubjectex. Refresh \_**](swbemobjectex-refresh-.md) " auf.

    ```VB
    objRefresher.Refresh
    ```

    

5.  Wenn Sie die Leistung überwachen und eine Sammlung im Aktualisierungs Objekt enthalten, durchlaufen Sie die Auflistungs Objekte.

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  Löschen Sie die Elemente aus dem Aktualisierungs Programm, indem Sie die Option " [**Swap. DeleteAll**](swbemrefresher-deleteall.md) " aufrufen oder bestimmte Elemente entfernen, indem Sie " [**Swap. Remove**](swbemrefresher-remove.md)" aufrufen.

Im folgenden VBScript-Codebeispiel wird gezeigt, wie ein einzelnes Objekt auf dem lokalen Computer aktualisiert wird. Das Skript erstellt einen Aktualisierungs Container und fügt eine Instanz eines Enumerators für [**Win32 \_ perfformatteddata \_ perfproc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) -Instanzen hinzu. Der [**Aktualisierungs**](swbemrefresher-refresh.md) Aufruf wird dreimal durchgeführt, um die Änderungen in der Eigenschaft " **prozentuprocessortime** " für Prozesse zu veranschaulichen, die mehr als einen Prozentsatz der Prozessorzeit verwenden.


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



Die [**Index**](swbemrefreshableitem-index.md) -Eigenschaft des zurückgegebenen " [**taubemfreshableitem**](swbemrefreshableitem.md) "-Objekts stellt den Index des-Objekts in der Aktualisierungs-Auflistung dar. Sie können die Eigenschaft ' [**Swap. isset**](swbemrefreshableitem-isset.md) ' der Eigenschaft ' Swap ' aufzurufen, um zu bestimmen, ob ein Element in einem Aktualisierungs Programm ein einzelnes Element oder eine Auflistung ist. Wenn Sie auf ein einzelnes Element zugreifen möchten, verwenden Sie die Eigenschaft " [**Swap. Object**](swbemrefreshableitem-object.md) ". Wenn Sie den Aufrufvorgang für " **Swap. Object**" nicht durchführen, schlägt das Skript fehl, wenn Sie versuchen, auf das Objekt zuzugreifen. Um auf eine Auflistung zuzugreifen, verwenden Sie die Eigenschaft " [**Swap. ObjectSet**](swbemrefreshableitem-objectset.md) ".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Leistungs Leistungsdaten-Klassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Zugreifen auf Leistungsdaten im Skript](accessing-performance-data-in-script.md)
</dt> <dt>

[WMI-Tasks: Leistungsüberwachung](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> </dl>

 

 
