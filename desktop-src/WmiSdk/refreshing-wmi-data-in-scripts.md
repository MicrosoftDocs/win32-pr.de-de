---
description: In Überwachungsskripts können Sie aufeinanderfolgende Aufrufe von GetObject vermeiden, indem Sie ein SWbemRefresher-Objekt verwenden. Das SWbemRefresher-Objekt ist ein Container, der mehrere WMI-Objekte enthalten kann, deren Daten in einem Aufruf aktualisiert werden können.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Aktualisieren von WMI-Daten in Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 969a97c6300ac256e08c79e4f4aaeaa8d05bda072a2c310812ce3b2061c791fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050448"
---
# <a name="refreshing-wmi-data-in-scripts"></a>Aktualisieren von WMI-Daten in Skripts

In Überwachungsskripts können Sie aufeinanderfolgende Aufrufe von **GetObject vermeiden,** indem Sie ein [**SWbemRefresher-Objekt**](swbemrefresher.md) verwenden. Das **SWbemRefresher-Objekt** ist ein Container, der mehrere WMI-Objekte enthalten kann, deren Daten in einem Aufruf aktualisiert werden können.

Die Verwendung [**eines SWbemRefresher-Objekts**](swbemrefresher.md) ist erforderlich, um genaue Daten aus WMI-Leistungsklassen wie [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) oder anderen vorinstallierten Klassen zu erhalten, die von [**Win32 \_ Perf abgeleitet werden.**](/windows/desktop/CIMWin32Prov/win32-perf)

Im folgenden Verfahren wird beschrieben, wie Daten in Skripts aktualisiert werden.

**So aktualisieren Sie Daten in Skripts**

1.  Rufen **Sie CreateObject** auf, um ein [**SWbemRefresher-Aktualisierungsobjekt**](swbemrefresher.md) zu erstellen.

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  Verbinden in den WMI-Namespace. Um vorinstallierte [**Win32 \_ Perf-Klassen zu**](/windows/desktop/CIMWin32Prov/win32-perf) verwenden, stellen Sie eine Verbindung mit dem Stamm **\\ cimv2 auf.**

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  Fügen Sie ein einzelnes -Objekt (rufen [**Sie SWbemRefresher.Add**](swbemrefresher-add.md)auf) oder eine -Auflistung (rufen [**Sie SWbemRefresher.AddEnum**](swbemrefresher-addenum.md)auf) zur Aktualisierung hinzu.

    Verwenden Sie die vorab berechneten Datenklassen, die von [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)abgeleitet wurden, z. B. [**Win32 \_ PerfFormattedData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) anstelle von [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk.**](./retrieving-raw-and-formatted-performance-data.md) Andernfalls müssen Sie die Werte für alle Eigenschaften berechnen, die keine einfachen Leistungsindikatoren sind.

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  Aktualisieren Sie die Daten einmal, um die anfänglichen Leistungsdaten zu erhalten.

    Rufen Sie entweder [**die SWbemRefresher.Refresh-Methode**](swbemrefresher-refresh.md) oder die generische [**SWbemObjectEx.Refresh-Methode \_**](swbemobjectex-refresh-.md) auf.

    ```VB
    objRefresher.Refresh
    ```

    

5.  Wenn Sie die Leistung überwachen und über eine Auflistung im Aktualisierungsobjekt verfügen, führen Sie eine Schleife durch die Auflistungsobjekte.

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  Löschen Sie die Elemente aus der Aktualisierung, indem Sie [**SWbemRefresher.DeleteAll**](swbemrefresher-deleteall.md) aufrufen oder bestimmte Elemente entfernen, indem [**Sie SwbemRefresher.Remove aufrufen.**](swbemrefresher-remove.md)

Das folgende VBScript-Codebeispiel zeigt, wie ein einzelnes -Objekt auf dem lokalen Computer aktualisiert wird. Das Skript erstellt einen Aktualisierungscontainer und fügt eine Instanz eines Enumerators für [**Win32 \_ PerfFormattedData \_ PerfProc \_ Process-Instanzen**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) hinzu. Der [**Refresh-Aufruf**](swbemrefresher-refresh.md) wird dreimal vorgenommen, um die Änderungen an der **PercentProcessorTime-Eigenschaft** für Prozesse zu veranschaulichen, die mehr als einen Prozent der Prozessorzeit verwenden.


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



Die [**Index-Eigenschaft**](swbemrefreshableitem-index.md) des zurückgegebenen [**SWbemRefreshableItem**](swbemrefreshableitem.md) stellt den Index des -Objekts in der Refresher-Auflistung dar. Sie können die [**SWbemRefreshableItem.IsSet-Eigenschaft**](swbemrefreshableitem-isset.md) aufrufen, um zu bestimmen, ob ein Element in einer Aktualisierung ein einzelnes Element oder eine Sammlung ist. Verwenden Sie für den Zugriff auf ein einzelnes Element die [**Eigenschaft SWbemRefreshableItem.Object.**](swbemrefreshableitem-object.md) Wenn Sie **SWbemRefreshableItem.Object** nicht aufrufen, schlägt das Skript fehl, wenn Sie versuchen, auf das Objekt zu zugreifen. Verwenden Sie für den Zugriff auf eine Sammlung die [**Eigenschaft SWbemRefreshableItem.ObjectSet.**](swbemrefreshableitem-objectset.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Leistungsindikatorklassen](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[Zugreifen auf Leistungsdaten in Skripts](accessing-performance-data-in-script.md)
</dt> <dt>

[WMI-Aufgaben: Leistungsüberwachung](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[Überwachen von Leistungsdaten](monitoring-performance-data.md)
</dt> </dl>

 

 
