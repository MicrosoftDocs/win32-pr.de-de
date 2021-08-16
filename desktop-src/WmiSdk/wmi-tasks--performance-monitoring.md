---
description: Verwenden Sie die WMI-Klassen, die Daten aus Leistungsindikatoren abrufen, um auf Daten zur Computerleistung zuzugreifen und diese zu aktualisieren.
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: 'WMI-Aufgaben: Leistungsüberwachung'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91302b0d6c6e13f86f275d755c5f4b6150de6a59dd400e47ed877d01f3fe876e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312056"
---
# <a name="wmi-tasks-performance-monitoring"></a>WMI-Aufgaben: Leistungsüberwachung

Verwenden Sie die WMI-Klassen, die Daten aus Leistungsindikatoren abrufen, um auf Daten zur Computerleistung zuzugreifen und diese zu aktualisieren. Weitere Beispiele finden Sie im TechNet ScriptCenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . Weitere Informationen finden Sie unter [Leistungsbibliotheken und WMI](performance-libraries-and-wmi.md) und [Überwachen von Leistungsdaten.](monitoring-performance-data.md)

Die in diesem Thema gezeigten Skriptbeispiele rufen Daten nur vom lokalen Computer ab. Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remotecomputern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)


Im folgenden Verfahren wird beschrieben, wie Ein Skript ausgeführt wird.

**So führen Sie ein Skript aus**

1.  Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung .vbs, z. *B.filename.vbs*. Stellen Sie sicher, dass ihr Text-Editor der Datei keine .txt Erweiterung hinzufüg.
2.  Öffnen Sie ein Eingabeaufforderungsfenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.
3.  Geben Sie an der Eingabeaufforderung **cscript filename.vbs** ein.
4.  Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie über eine Eingabeaufforderung mit erhöhten Rechten ausführen. Einige Ereignisprotokolle, z. B. das Sicherheitsereignisprotokoll, können durch Benutzerzugriffssteuerungen (User Access Controls, UAC) geschützt werden.

> [!Note]  
> Standardmäßig zeigt cscript die Ausgabe eines Skripts im Eingabeaufforderungsfenster an. Da WMI-Skripts große Mengen von Ausgaben erzeugen können, sollten Sie die Ausgabe an eine Datei umleiten. Geben Sie **cscript filename.vbs > outfile.txt** an der Eingabeaufforderung ein, um die Ausgabe des *filename.vbs* Skripts anoutfile.txt *umzuleiten.*

 

In der folgenden Tabelle sind Skriptbeispiele aufgeführt, die zum Abrufen verschiedener Datentypen vom lokalen Computer verwendet werden können.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vorgehensweisen</th>
<th>WMI-Klassen oder -Methoden</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... Rufen Sie die Leistungsindikatordaten ab, die im Perfmon-Hilfsprogramm in einem Skript angezeigt werden?</td>
<td>Verwenden Sie Klassen mit Namen, die mit &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a> &quot; beginnen, z. <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>B. Win32_PerfFormattedData_PerfProc_Process</strong></a>. Eigenschaften mit Namen wie <strong>PageFileBytes</strong> entsprechen Leistungsindikatoren, die in Perfmon angezeigt werden. Die &quot; Win32_PerfFormattedData Klassen berechnen die &quot; endgültigen Werte von Leistungsindikatoren für Sie.<br/></td>
</tr>
<tr class="even">
<td>... Erhalten Sie laufende Leistungsdaten für einen einzelnen Prozess, ein Laufwerk und andere Daten?</td>
<td>Verwenden Sie die <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> oder die entsprechende formatierte <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Leistungsindikatorklasse</a> und die <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_-Methode.</strong></a> Weitere Informationen finden Sie unter <a href="scripting-with-swbemobject.md">Skripterstellung mit SWbemObject.</a><br/> Verwenden Sie in C++ <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher::AddObjectByPath</strong></a> und <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher::Refresh</strong></a>. Weitere Informationen finden Sie unter <a href="monitoring-performance-data.md">Überwachen von Leistungsdaten.</a><br/> Das folgende Skript wird ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell zu beenden, verwenden Sie Task-Manager, um den Prozess zu beenden. Um sie programmgesteuert zu beenden, verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate-Methode</strong></a> in der <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process-Klasse.</strong></a><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<td>... Erhalten Sie laufende Leistungsdaten für alle Prozesse ohne wiederholte Abrufe?</td>
<td><p>Verwenden Sie Klassen mit Namen, die mit &quot; Win32_PerfFormattedData &quot; und einem <a href="swbemrefresher.md"><strong>SWbemRefresher-Objekt</strong></a> beginnen. Die Aktualisierung enthält die -Objekte, sodass Sie die Auflistung nicht wiederholt abrufen müssen. Zum Berechnen der Leistungsdaten sind mindestens zwei Werte erforderlich, da die meisten Leistungsindikatoren Ratenindikatoren sind. Wenn Sie die Aktualisierungsdaten zum ersten Mal anzeigen, sind sie leer.</p>
<p>Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell zu beenden, verwenden Sie Task-Manager, um den Prozess zu beenden. Um sie programmgesteuert zu beenden, verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate-Methode</strong></a> in der <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process-Klasse.</strong></a></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<td>... Leistungsdaten für Prozesse Windows 2000 abrufen und berechnen?</td>
<td><p>Verwenden Sie die &quot; Win32_PerfRawData &quot; Klassen, z. <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>B. Win32_PerfRawData_PerfProc_Process</strong></a>. Abrufen der Eigenschaftsdaten, z. B. <strong>PercentProcessorTime,</strong>zweimal für einen bestimmten Prozess. Suchen Sie nach der Formel, die im <a href="countertype-qualifier.md"><strong>CounterType-Qualifizierer</strong></a> für die Eigenschaft angegeben ist, und berechnen Sie sie. Der CounterType im Beispiel ist <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>. Weitere Informationen finden Sie unter <a href="monitoring-performance-data.md">Überwachen von Leistungsdaten.</a></p>
<p>Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell zu beenden, verwenden Sie Task-Manager, um den Prozess zu beenden. Um sie programmgesteuert zu beenden, verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate-Methode</strong></a> in der <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process-Klasse.</strong></a></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Aufgaben für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[WMI C++-Anwendungsbeispiele](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
