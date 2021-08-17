---
description: Das SWbemObject-Skriptobjekt ist das generische WMI-Objekt, das Eigenschaften und Methoden definiert, die unabhängig vom spezifischen WMI-Objekt verwendet werden können, an das das SWbemObject-Objekt gebunden ist.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Skripterstellung mit SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d6ba0cccca8fcd62af490aa91ab1cc965fdad4d3682d99a8fda52151135500ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739696"
---
# <a name="scripting-with-swbemobject"></a>Skripterstellung mit SWbemObject

Das [**SWbemObject-Skriptobjekt**](swbemobject.md) ist das generische WMI-Objekt, das Eigenschaften und Methoden definiert, die unabhängig vom spezifischen WMI-Objekt verwendet werden können, an das das **SWbemObject-Objekt** gebunden ist. Alle WMI-Objekte, z. B. eine Instanz von [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) oder eine andere WMI-Datenklasse, werden durch [**SWbemObject**](swbemobject.md) dargestellt und können die allgemeinen **SWbemObject-Eigenschaften** und -Methoden zusätzlich zu ihren eigenen speziellen Eigenschaften und Methoden verwenden.

Verwenden Sie beispielsweise das folgende Skript, um alle Instanzen eines [**\_ Win32-Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) durch Aufrufen der [**SWbemObject.Instances-Methode zu \_**](swbemobject-instances-.md) erhalten. ClsobjProcess stellt sowohl die **Win32 \_ Process-Klassendefinition** als auch ein [**SWbemObject dar.**](swbemobject.md)


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



Im folgenden Beispiel wird eine bestimmte Instanz des [**\_ Win32-Diensts,**](/windows/desktop/CIMWin32Prov/win32-service) die den Alerter-Dienst darstellt, und in objAlerter gespeichert. Anschließend können Sie [**entweder SWbemObject-Methoden**](swbemobject.md) wie WScript.Echo objAlerter.Path oder von der Datenklasse definierte Methoden aufrufen, z.B. \_ WScript.Echo objAlerter.State. objAlerter, das sowohl eine Instanz des Win32-Diensts als \_ auch ein **SWbemObject darstellt.**


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



Der Aufruf von [**SWbemObject.Instances \_**](swbemobject-instances-.md) erhält ein weiteres generisches WMI-Skriptobjekt, [**SWbemObjectSet.**](swbemobjectset.md) Wie gezeigt, kann **das SWbemObjectSet-Objekt** als Auflistung behandelt [werden.](accessing-a-collection.md)


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



Sie können die [**SWbemObject-Methoden**](swbemobject.md) identifizieren, da sie alle mit einem Unterstrich ( ) enden, z. B. \_ [**SWbemObject.Instances \_**](swbemobject-instances-.md).

[**SWbemObjectEx**](swbemobjectex.md) erweitert die Eigenschaften von [**SWbemObject**](swbemobject.md). Beispielsweise können Sie jetzt die Daten eines beliebigen WMI-Objekts, z. B. einer Instanz des [**\_ Win32-Prozesses,**](/windows/desktop/CIMWin32Prov/win32-process)durch einen Aufruf von [**SWbemObjectEx.Refresh aktualisieren. \_**](swbemobjectex-refresh-.md)

Das folgende Beispiel zeigt, wie die Fehlerdaten der Systemprozessseite alle fünf Sekunden aktualisiert werden können.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



Weitere Informationen zum Aktualisieren von Daten mithilfe eines [**SWbemRefresher-Objekts**](swbemrefresher.md) finden Sie unter Aktualisieren von [WMI-Daten in Skripts.](refreshing-wmi-data-in-scripts.md)

Mit [**\_ SWbemObject.Put**](swbemobject-put-.md) und [**PutAsync \_**](swbemobject-putasync-.md) können Sie Änderungen in ein beliebiges WMI-Objekt zurückschreiben. Diese Methoden commiten nur Änderungen an einem Objekt in dem Namespace, in dem das Objekt erstellt wurde. Sie können das Objekt mithilfe von [**SWbemServicesEx.Put**](swbemservicesex-put.md) oder [**SWbemServicesEx.PutAsync**](swbemservicesex-putasync.md)in einen anderen Namespace schreiben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skripterstellungs-API für WMI](scripting-api-for-wmi.md)
</dt> <dt>

[Erstellen eines WMI-Skripts](creating-a-wmi-script.md)
</dt> <dt>

[Aktualisieren einer gesamten Instanz](updating-an-entire-instance.md)
</dt> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 
