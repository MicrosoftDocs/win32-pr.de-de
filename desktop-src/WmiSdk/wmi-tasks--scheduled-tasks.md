---
description: Mit geplanten WMI-Tasks können Sie Informationen zu geplanten Aufgaben erstellen und abrufen. Weitere Beispiele finden Sie im TechNet ScriptCenter unter https://www.microsoft.com/technet .
ms.assetid: 62151fe8-8880-43f2-b456-628bd9c7cc1c
ms.tgt_platform: multiple
title: 'WMI-Aufgaben: Geplante Aufgaben'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee4fcf193296d5c474987a3a99877b3bfb43868f79527200893303df351920cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738839"
---
# <a name="wmi-tasks-scheduled-tasks"></a>WMI-Aufgaben: Geplante Aufgaben

Mit geplanten WMI-Tasks können Sie Informationen zu geplanten Aufgaben erstellen und abrufen. Weitere Beispiele finden Sie im TechNet ScriptCenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

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
<td>... Geplante Aufgaben mithilfe von Skripts erstellen?</td>
<td>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob-Klasse</strong></a> und die <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create-Methode.</strong></a> Wenn Sie Schwierigkeiten haben, diese Aufgabe mit Windows 7 oder höher zu bearbeiten, lesen Sie den Abschnitt <strong>Win32_ScheduledJob</strong> Hinweise. Wahrscheinlich verhindern Ihre Einstellungen die Verwendung der -Klasse.<br/> <span data-codelanguage="VisualBasic"></span>
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
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
JobID = &quot;Test&quot;
Set objNewJob = objWMIService.Get(&quot;Win32_ScheduledJob&quot;)
errJobCreate = objNewJob.Create _
    (&quot;Notepad.exe&quot;, &quot;********143000.000000-420&quot;, True , 1 OR 4 OR 16, ,True, JobId) 
If errJobCreate = 0 Then
    WScript.Echo &quot;Job created successfully: &quot; & VBNewLine _
        & &quot;Notepad.exe scheduled to run repeately at 14.30 (2:30 P.M.) PST&quot; & VBNewLine _
        & &quot;on Mon, Wed, and Fri.&quot;
Else
    WScript.Echo &quot;Job not created. Error code = &quot; & errJobCreate
End If</code></pre></td>
</tr>
</tbody>
</table>

<p>In der Zeichenfolge &quot; "**143000.000000-420" &quot; (wird im <em>StartTime-Parameterwert</em> der <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create-Methode</strong></a> verwendet) &quot; gibt "**143000.000000" &quot; an, dass der Task bei 14,30 (14:30 Uhr) beginnt und &quot; -420 &quot; die Zeitzone angibt. Die Zeitzonennummer ist die aktuelle Verschiebung der Ortszeitübersetzung. Die Verschiebung ist der Unterschied zwischen der UTC-Zeit und der Ortszeit. Multiplizieren Sie zum Berechnen der Verschiebung für Ihre Zeitzone die Anzahl der Stunden, denen Ihre Zeitzone voraus oder hinter Greenwich Mean Time (GMT) liegt, mit 60 (verwenden Sie eine positive Zahl für die Anzahl der Stunden, wenn Ihre Zeitzone vor GMT liegt, und eine negative Zahl, wenn Ihre Zeitzone hinter GMT liegt). Fügen Sie ihrer Berechnung eine zusätzliche 60 hinzu, wenn Ihre Zeitzone Sommerzeit verwendet. Beispielsweise liegt die Pacific Standard Time-Zone acht Stunden hinter GMT, daher entspricht die Abweichung -420 (-8 * 60 + 60), wenn die Sommerzeit verwendet wird, und -480 (-8 * 60), wenn die Sommerzeit nicht verwendet wird. Sie können auch den Wert des Bias bestimmen, indem Sie die Bias-Eigenschaft der <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone-Klasse</strong></a> abfragen.</p></td>
</tr>
<tr class="even">
<td>... gibt eine Liste aller geplanten Aufgaben auf einem Computer zurück?</td>
<td><p>Verwenden <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong></strong></a> Sie die Win32_ScheduledJob-Klasse. Beachten Sie, dass diese Klasse nur Aufträge zurückgeben kann, die entweder mit einem Skript oder AT.exe erstellt werden. Es können keine Informationen zu Aufträgen zurückgegeben werden, die vom Assistenten für geplante Aufgaben erstellt oder geändert wurden.</p>
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
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colScheduledJobs = objWMIService.ExecQuery (&quot;Select * from Win32_ScheduledJob&quot;)
For Each objJob in colScheduledJobs
    Wscript.Echo &quot;Command: &quot; & objJob.Command & VBNewLine _
    & &quot;Days Of Month: &quot; & objJob.DaysOfMonth & VBNewLine _
    & &quot;Days Of Week: &quot; & objJob.DaysOfWeek & VBNewLine _
    & &quot;Description: &quot; & objJob.Description & VBNewLine _
    & &quot;Elapsed Time: &quot; & objJob.ElapsedTime & VBNewLine _
    & &quot;Install Date: &quot; & objJob.InstallDate & VBNewLine _
    & &quot;Interact with Desktop: &quot; & objJob.InteractWithDesktop & VBNewLine _
    & &quot;Job ID: &quot; & objJob.JobId & VBNewLine _
    & &quot;Job Status: &quot; & objJob.JobStatus & VBNewLine _
    & &quot;Name: &quot; & objJob.Name & VBNewLine _
    & &quot;Notify: &quot; & objJob.Notify & VBNewLine _
    & &quot;Owner: &quot; & objJob.Owner & VBNewLine _
    & &quot;Priority: &quot; & objJob.Priority & VBNewLine _
    & &quot;Run Repeatedly: &quot; & objJob.RunRepeatedly & VBNewLine _
    & &quot;Start Time: &quot; & objJob.StartTime & VBNewLine _
    & &quot;Status: &quot; & objJob.Status & VBNewLine _
    & &quot;Time Submitted: &quot; & objJob.TimeSubmitted & VBNewLine _
    & &quot;Until Time: &quot; & objJob.UntilTime
Next</code></pre></td>
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

 

