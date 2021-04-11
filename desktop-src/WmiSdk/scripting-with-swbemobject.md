---
description: Das Skript Objekt von WS-Objekten ist das generische WMI-Objekt, das die Eigenschaften und Methoden definiert, die unabhängig von dem spezifischen WMI-Objekt verwendet werden können, an das das errbemubject-Objekt gebunden ist.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Skripterstellung mit "errbemuject"
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ce9a48779b13f1b1917ad189b2297b60329ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131008"
---
# <a name="scripting-with-swbemobject"></a>Skripterstellung mit "errbemuject"

Das [**Skript Objekt**](swbemobject.md) von WS-Objekten ist das generische WMI-Objekt, das die Eigenschaften und Methoden definiert, die unabhängig von dem spezifischen WMI-Objekt verwendet werden können, an das das **errbemubject** -Objekt gebunden ist. Alle WMI-Objekte, wie z. b. eine Instanz des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) oder eine beliebige andere WMI-Datenklasse, werden von " [**errbewbject**](swbemobject.md) " dargestellt und können zusätzlich zu ihren eigenen speziellen Eigenschaften und Methoden die allgemeinen Eigenschaften und Methoden von " **errbemubject** " verwenden.

Verwenden Sie z. b. das folgende Skript, um alle Instanzen eines [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process) zu erhalten, indem Sie die Methode " [**\_ errbemubject. Instance**](swbemobject-instances-.md) " aufrufen. Der clsobjprocess stellt sowohl die **Win32- \_ Prozess** Klassendefinition als auch ein- [**Austausch Objekt**](swbemobject.md)dar.


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



Im folgenden Beispiel wird eine bestimmte Instanz des [**Win32- \_ Dienstanbieter**](/windows/desktop/CIMWin32Prov/win32-service) abgerufen, die den alingdienst darstellt und in objalder gespeichert ist. Sie können dann entweder die " [**errbewbject**](swbemobject.md) "-Methoden (z. b. "Wscript. Echo objalken. Path") \_ oder die von der Datenklasse definierten Methoden (z. b. WScript. Echo objalen. State) aufzurufen. objalken, der sowohl eine Instanz des Win32 \_ -Dienstanbieter als auch ein **errbefubject** darstellt.


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



Der Aufrufen von " [**errbewbject. \_ instance**](swbemobject-instances-.md) " erhält ein anderes generisches WMI-Skript Objekt, " [**errbewbjectset**](swbemobjectset.md)". Wie gezeigt, kann das Objekt " **errbemubjectset** " als [Sammlung](accessing-a-collection.md)behandelt werden.


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



Sie können die " [**errbemubject**](swbemobject.md) "-Methoden ermitteln, da Sie alle auf einen Unterstrich ( \_ ) enden, z. b. " [**errbemubject. Instance \_**](swbemobject-instances-.md)".

Die Eigenschaften von "errbemubject" [](swbemobject.md)werden von " [**errbemubjectex**](swbemobjectex.md) " erweitert. Beispielsweise können Sie jetzt die Daten eines beliebigen WMI-Objekts (z. b. eine Instanz des [**Win32- \_ Prozesses**](/windows/desktop/CIMWin32Prov/win32-process)) durch einen Aufrufen von " [**errbewbjectex. Refresh \_**](swbemobjectex-refresh-.md)" aktualisieren.

Im folgenden Beispiel wird gezeigt, wie die Fehler Daten der System Prozess Seite alle fünf Sekunden aktualisiert werden können.


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



Weitere Informationen zum Aktualisieren von Daten mit einem " [**Swap**](swbemrefresher.md) "-Objekt finden Sie unter Aktualisieren von [WMI-Daten in Skripts](refreshing-wmi-data-in-scripts.md).

Mit " [**Swap. Put \_**](swbemobject-put-.md) " und " [**putasync \_**](swbemobject-putasync-.md) " können Sie Änderungen zurück in ein beliebiges WMI-Objekt schreiben. Diese Methoden übertragen nur Änderungen an einem Objekt im Namespace, in dem das Objekt erstellt wurde. Sie können das Objekt mithilfe von " [**scobemservicesex. Put**](swbemservicesex-put.md) " oder " [**scobemservicesex. putasync**](swbemservicesex-putasync.md)" in einen anderen Namespace schreiben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Skript-API für WMI](scripting-api-for-wmi.md)
</dt> <dt>

[Erstellen eines WMI-Skripts](creating-a-wmi-script.md)
</dt> <dt>

[Aktualisieren einer gesamten Instanz](updating-an-entire-instance.md)
</dt> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 
