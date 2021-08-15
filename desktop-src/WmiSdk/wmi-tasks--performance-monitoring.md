---
description: Verwenden Sie die WMI-Klassen, die Daten aus Leistungsindikatoren abrufen, um auf Daten zur Computerleistung zu zugreifen und diese zu aktualisieren.
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

Verwenden Sie die WMI-Klassen, die Daten aus Leistungsindikatoren abrufen, um auf Daten zur Computerleistung zu zugreifen und diese zu aktualisieren. Weitere Beispiele finden Sie im TechNet ScriptCenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . Weitere Informationen finden Sie unter [Leistungsbibliotheken und WMI](performance-libraries-and-wmi.md) und [Überwachen von Leistungsdaten.](monitoring-performance-data.md)

Die in diesem Thema gezeigten Skriptbeispiele beziehen nur Daten vom lokalen Computer. Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remotecomputern finden Sie unter Herstellen einer Verbindung [mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)


Im folgenden Verfahren wird das Ausführen eines Skripts beschrieben.

**So führen Sie ein Skript aus**

1.  Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung .vbs, z. *B.filename.vbs*. Stellen Sie sicher, dass Ihr Text-Editor der Datei .txt erweiterung hinzufüge.
2.  Öffnen Sie ein Eingabeaufforderungsfenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.
3.  Geben **Sie cscript filename.vbs** eingabeaufforderung ein.
4.  Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie über eine Eingabeaufforderung mit erhöhten Rechten ausführen. Einige Ereignisprotokollen, z. B. das Sicherheitsereignisprotokoll, können durch Benutzerzugriffssteuerungen (User Access Controls, UAC) geschützt werden.

> [!Note]  
> Standardmäßig zeigt cscript die Ausgabe eines Skripts im Eingabeaufforderungsfenster an. Da WMI-Skripts große Mengen an Ausgabe erzeugen können, sollten Sie die Ausgabe an eine Datei umleiten. Geben **Sie cscript filename.vbs > outfile.txt** eingabeaufforderung ein, um  die Ausgabe des skriptsfilename.vbsan *outfile.txt.*

 

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
<td>... Die Leistungsindikatordaten abrufen, die im Perfmon-Hilfsprogramm in einem Skript angezeigt werden?</td>
<td>Verwenden Sie Klassen mit Namen, die mit Win32_PerfFormattedData &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes"></a> &quot; beginnen, z. <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>B. Win32_PerfFormattedData_PerfProc_Process</strong></a>. Eigenschaften mit Namen wie <strong>PageFileBytes</strong> entsprechen Leistungsindikatoren, die in Perfmon angezeigt werden. Die &quot; Win32_PerfFormattedData &quot; berechnen die endgültigen Werte der Leistungsindikatoren für Sie.<br/></td>
</tr>
<tr class="even">
<td>... Erhalten Sie leistungsorientierte Leistungsdaten für einen einzelnen Prozess, ein Laufwerk und andere Daten?</td>
<td>Verwenden Sie <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> oder die entsprechende formatierte <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Leistungsindikatorklasse</a> und die <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> Methode. Weitere Informationen finden Sie unter <a href="scripting-with-swbemobject.md">Skripterstellung mit SWbemObject</a>.<br/> Verwenden Sie in C++ <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher::AddObjectByPath</strong></a> und <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher::Refresh.</strong></a> Weitere Informationen finden Sie unter <a href="monitoring-performance-data.md">Überwachen von Leistungsdaten.</a><br/> Das folgende Skript wird ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell zu beenden, verwenden Sie Task-Manager, um den Prozess zu beenden. Verwenden Sie zum programmgesteuerten Beenden die <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate-Methode</strong></a> in der <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> Klasse.<br/> <span data-codelanguage="VisualBasic"></span>
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
<td>... Erhalten Sie ohne wiederholte Abrufe leistungsbasierte Leistungsdaten für alle Prozesse?</td>
<td><p>Verwenden Sie Klassen mit Namen, die mit Win32_PerfFormattedData &quot; &quot; und einem <a href="swbemrefresher.md"><strong>SWbemRefresher-Objekt</strong></a> beginnen. Die Auffrischung enthält die -Objekte, sodass Sie die Auflistung nicht wiederholt erhalten müssen. Mindestens zwei Werte sind erforderlich, um Leistungsdaten zu berechnen, da die meisten Leistungsindikatoren Rate Counters sind. Wenn Sie die Aktualisierungsdaten zum ersten Mal anzeigen, sind sie leer.</p>
<p>Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell zu beenden, verwenden Sie Task-Manager, um den Prozess zu beenden. Verwenden Sie zum programmgesteuerten Beenden die <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate-Methode</strong></a> in der <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> Klasse.</p>
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
<td>... Leistungsdaten für Prozesse in Windows 2000 erhalten und berechnen?</td>
<td><p>Verwenden Sie &quot; Win32_PerfRawData &quot; Klassen, z. <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>B. Win32_PerfRawData_PerfProc_Process</strong></a>. Sie können die Eigenschaftsdaten, z. <strong>B. PercentProcessorTime,</strong>zweimal für einen bestimmten Prozess erhalten. Suchen Sie nach der <a href="countertype-qualifier.md"><strong></strong></a> Formel, die im CounterType-Qualifizierer für die Eigenschaft angegeben ist, und berechnen Sie sie. Der CounterType im Beispiel ist <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>. Weitere Informationen finden Sie unter <a href="monitoring-performance-data.md">Überwachen von Leistungsdaten.</a></p>
<p>Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell zu beenden, verwenden Sie Task-Manager, um den Prozess zu beenden. Verwenden Sie zum programmgesteuerten Beenden die <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate-Methode</strong></a> in der <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> Klasse.</p>
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

[Beispiele für WMI-C++-Anwendungen](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
