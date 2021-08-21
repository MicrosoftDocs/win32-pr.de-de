---
description: WMI-Tasks für Prozesse rufen Informationen ab, z. B. das Konto, unter dem ein Prozess ausgeführt wird. Sie können Aktionen wie das Erstellen von Prozessen ausführen. Weitere Beispiele finden Sie im TechNet ScriptCenter unter https://www.microsoft.com/technet .
ms.assetid: 2ae7c302-ab8b-4150-8ece-ffb66374b3f7
ms.tgt_platform: multiple
title: 'WMI-Tasks: Prozesse '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0847179cc67635ab872f71d79ed77c337ec6044291db13f5d1ca48101fc5dbad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049888"
---
# <a name="wmi-tasks-processes"></a>WMI-Tasks: Prozesse 

WMI-Tasks für Prozesse rufen Informationen ab, z. B. das Konto, unter dem ein Prozess ausgeführt wird. Sie können Aktionen wie das Erstellen von Prozessen ausführen. Weitere Beispiele finden Sie im TechNet ScriptCenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

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
<td>... Eine Anwendung in einem ausgeblendeten Fenster ausführen?</td>
<td>Rufen Sie die Anwendung über ein Skript auf, das die <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>klassen Win32_Process</strong></a> und <a href="/windows/desktop/CIMWin32Prov/win32-processstartup"><strong>Win32_ProcessStartup</strong></a> verwendet.<br/> <span data-codelanguage="VisualBasic"></span>
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
<td><pre><code>Const HIDDEN_WINDOW = 0
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objStartup = objWMIService.Get(&quot;Win32_ProcessStartup&quot;)
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject(&quot;winmgmts:root\cimv2:Win32_Process&quot;)
errReturn = objProcess.Create( &quot;Notepad.exe&quot;, null, objConfig, intProcessID)</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$startup=[wmiclass]&quot;Win32_ProcessStartup&quot;
$startup.Properties[&#39;ShowWindow&#39;].value=$False
([wmiclass]&quot;win32_Process&quot;).create(&#39;notepad.exe&#39;,&#39;C:\&#39;,$Startup)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... ermitteln, welche Skripts auf dem lokalen Computer ausgeführt werden?</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> -Klasse, und geben Sie alle Prozesse mit dem Namen Cscript.exe oder Wscript.exe zurück. Um die einzelnen Skripts zu bestimmen, die in diesen Prozessen ausgeführt werden, überprüfen Sie den Wert der <strong>CommandLine-Eigenschaft.</strong></p>
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
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\CIMV2&quot;) 
Set colItems = objWMIService.ExecQuery(&quot;SELECT * FROM Win32_Process&quot; & _
           &quot; WHERE Name = &#39;cscript.exe&#39;&quot; & &quot; OR Name = &#39;wscript.exe&#39;&quot;,,48) 
For Each objItem in colItems 
    Wscript.Echo &quot;-------------------------------------------&quot;
    Wscript.Echo &quot;CommandLine: &quot; & objItem.CommandLine
    Wscript.Echo &quot;Name: &quot; & objItem.Name
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
Get-WmiObject -Class &quot;Win32_Process&quot; -ComputerName &quot;.&quot; | `
     where {($_.name -eq &#39;cscript.exe&#39;) -or ($_.name -eq &#39;wscript.exe&#39;) } | `
     Format-List -Property CommandLine, Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... ermitteln Sie den Kontonamen, unter dem ein Prozess ausgeführt wird?</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process-Klasse</strong></a> und die <a href="/windows/desktop/CIMWin32Prov/getowner-method-in-class-win32-process"><strong>GetOwner-Methode.</strong></a></p>
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
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    colProperties = objProcess.GetOwner( strNameOfUser,strUserDomain)
    Wscript.Echo &quot;Process &quot; & objProcess.Name & &quot; is owned by &quot; & strUserDomain & &quot;\&quot; & strNameOfUser & &quot;.&quot;
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -class win32_process -ComputerName &quot;.&quot; | ForEach-Object { $_.GetOwner() | Select -Property domain, user }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... ändern Sie die Priorität eines ausgeführten Prozesses?</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process-Klasse</strong></a> und die <a href="/windows/desktop/CIMWin32Prov/setpriority-method-in-class-win32-process"><strong>SetPriority-Methode.</strong></a></p>
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
<td><pre><code>Const ABOVE_NORMAL = 32768
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcesses = objWMIService.ExecQuery (&quot;Select * from Win32_Process Where Name = &#39;Notepad.exe&#39;&quot;)
For Each objProcess in colProcesses
    objProcess.SetPriority(ABOVE_NORMAL) 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$ABOVE_NORMAL = 32768
$strComputer = &quot;.&quot;
$colProcesses = Get-WmiObject -Class Win32_Process -ComputerName $strComputer | Where-Object { $_.name -eq &#39;Notepad.exe&#39; }
foreach ($objProcess in $colProcesses) { $objProcess.SetPriority($ABOVE_NORMAL) }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... beenden Sie einen Prozess mithilfe eines Skripts?</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process-Klasse</strong></a> und die <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate-Methode.</strong></a></p>
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
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process Where Name = &#39;Notepad.exe&#39;&quot;)
For Each objProcess in colProcessList
    objProcess.Terminate()
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colProcesses = Get-WmiObject -Class Win32_Process -ComputerName $strComputer | Where-Object { $_.name -eq &#39;Notepad.exe&#39; }
foreach ($objProcess in $colProcesses) { $objProcess.Terminate() }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... ermitteln, wie viel Prozessorzeit und Arbeitsspeicher die einzelnen Prozesse verwenden?</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> Klasse und Eigenschaften wie <strong>KernelModeTime,</strong> <strong>WorkingSetSize,</strong> <strong>PageFileUsage</strong>und <strong>PageFaults.</strong></p>
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
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcesses = objWMIService.ExecQuery(&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcesses
    Wscript.Echo &quot;Process: &quot; & objProcess.Name
    sngProcessTime = (CSng(objProcess.KernelModeTime) + CSng(objProcess.UserModeTime)) / 10000000
    Wscript.Echo &quot;Processor Time: &quot; & sngProcessTime
    Wscript.Echo &quot;Process ID: &quot; & objProcess.ProcessID
    Wscript.Echo &quot;Working Set Size: &quot; & objProcess.WorkingSetSize
    Wscript.Echo &quot;Page File Size: &quot; & objProcess.PageFileUsage
    Wscript.Echo &quot;Page Faults: &quot; & objProcess.PageFaults
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
Get-WmiObject -Class &quot;Win32s_Process&quot; -ComputerName $strComputer | `
     Format-List -Property Name, KernelModeTime, UserModeTime, ProcessID, WorkingSetSize, PageFileUsage, PageFaults</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... erfahren Sie, welche Anwendungen auf einem Remotecomputer ausgeführt werden?</td>
<td><p>Verwenden <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong></strong></a> Sie die Win32_Process-Klasse.</p>
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
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process: &quot; & objProcess.Name 
    Wscript.Echo &quot;Process ID: &quot; & objProcess.ProcessID 
    Wscript.Echo &quot;Thread Count: &quot; & objProcess.ThreadCount 
    Wscript.Echo &quot;Page File Size: &quot; & objProcess.PageFileUsage 
    Wscript.Echo &quot;Page Faults: &quot; & objProcess.PageFaults 
    Wscript.Echo &quot;Working Set Size: &quot; & objProcess.WorkingSetSize 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
get-wmiObject -class Win32_Process -Namespace &quot;root\cimv2&quot; -ComputerName $strComputer | `
   Format-list Name, ProcessID, ThreadCount, PageFileUsage, PageFaults, WorkingSetSize</code></pre></td>
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

 

