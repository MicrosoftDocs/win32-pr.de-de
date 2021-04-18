---
description: Verwenden Sie die WMI-Klassen, die Daten aus Leistungsindikatoren abrufen, um auf Daten über die Computerleistung zuzugreifen und diese zu aktualisieren.
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: 'WMI-Tasks: Leistungsüberwachung'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbb254e14280bec5a928bdc32aaa9a3e03c7a4f4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106361253"
---
# <a name="wmi-tasks-performance-monitoring"></a>WMI-Tasks: Leistungsüberwachung

Verwenden Sie die WMI-Klassen, die Daten aus Leistungsindikatoren abrufen, um auf Daten über die Computerleistung zuzugreifen und diese zu aktualisieren. Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . Weitere Informationen finden Sie unter [Leistungs Bibliotheken und WMI](performance-libraries-and-wmi.md) und über [Wachen von Leistungsdaten](monitoring-performance-data.md).

In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen. Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).


Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.

**So führen Sie ein Skript aus**

1.  Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*. Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.
2.  Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.
3.  Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.
4.  Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen. Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.

> [!Note]  
> Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an. Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten. Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.

 

In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vorgehensweisen</th>
<th>WMI-Klassen oder-Methoden</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... Abrufen der Leistungsdaten, die im Dienstprogramm "Perfmon" in einem Skript angezeigt werden?</td>
<td>Verwenden Sie Klassen, deren Namen mit &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a>beginnen &quot; , z. b. <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>. Eigenschaften mit Namen wie <strong>pagefilebytes</strong> entsprechen Leistungsindikatoren, die in Perfmon angezeigt werden. Die &quot; Win32_PerfFormattedData &quot; Klassen berechnen die Endwerte der Zähler für Sie.<br/></td>
</tr>
<tr class="even">
<td>... erhalten Sie fortlaufende Leistungsdaten für einen einzelnen Prozess, ein Laufwerk und andere Daten?</td>
<td>Verwenden Sie die <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> oder die entsprechende formatierte <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Leistungs Leistungs</a> -und <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> Methode. Weitere Informationen finden Sie unter <a href="scripting-with-swbemobject.md">Skripterstellung mit "Swap</a>".<br/> Verwenden Sie in C++ <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>iwbemconfigurerefresher:: addobjectbypath</strong></a> und <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>iwbemrefresh Sher:: Refresh</strong></a>. Weitere Informationen finden Sie unter über <a href="monitoring-performance-data.md">Wachen von Leistungsdaten</a>.<br/> Das folgende Skript wird so lange ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell anzuhalten, verwenden Sie den Task-Manager, um den Prozess zu unterbinden. Verwenden Sie zum Programm <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>gesteuerten beenden die Beendigungs Methode in</strong></a> der <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> -Klasse.<br/> <span data-codelanguage="VisualBasic"></span>
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
<td>... erhalten Sie fortlaufende Leistungsdaten für alle Prozesse ohne wiederholtes abrufen?</td>
<td><p>Verwenden Sie Klassen, die Namen haben, die mit Win32_PerfFormattedData beginnen, &quot; &quot; und ein <a href="swbemrefresher.md"><strong>Swap</strong></a> -Aktualisierungs-Objekt. Das Aktualisierungs Programm enthält die Objekte, sodass Sie die Auflistung nicht wiederholt erhalten müssen. Es sind mindestens zwei Werte erforderlich, um Leistungsdaten zu berechnen, da die meisten Leistungsindikatoren Raten Indikatoren sind. Wenn Sie die Aktualisierungsdaten zum ersten Mal anzeigen, ist es leer.</p>
<p>Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell anzuhalten, verwenden Sie den Task-Manager, um den Prozess zu unterbinden. Verwenden Sie zum Programm <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>gesteuerten beenden die Beendigungs Methode in</strong></a> der <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> -Klasse.</p>
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
<td>... erhalten und berechnen Sie Leistungsdaten für Prozesse unter Windows 2000?</td>
<td><p>Verwenden Sie die &quot; Win32_PerfRawData &quot; Klassen, z. b. <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>. Die Eigenschaften Daten, z. b. " <strong>prozesprozessortime</strong>", werden für einen bestimmten Prozess zweimal angezeigt. Suchen Sie die im <a href="countertype-qualifier.md"><strong>CounterType</strong></a> -Qualifizierer für die Eigenschaft angegebene Formel, und berechnen Sie. Der CounterType im Beispiel ist <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>. Weitere Informationen finden Sie unter über <a href="monitoring-performance-data.md">Wachen von Leistungsdaten</a>.</p>
<p>Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird. Um das Skript manuell anzuhalten, verwenden Sie den Task-Manager, um den Prozess zu unterbinden. Verwenden Sie zum Programm <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>gesteuerten beenden die Beendigungs Methode in</strong></a> der <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> -Klasse.</p>
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

[WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[WMI C++ Anwendungsbeispiele](wmi-c---application-examples.md)
</dt> <dt>

[Technet scriptcenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
