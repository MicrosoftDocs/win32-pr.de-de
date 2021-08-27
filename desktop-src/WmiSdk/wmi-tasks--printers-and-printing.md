---
description: WMI-Aufgaben für Drucker und Drucken verwalten und erhalten Daten zu Druckern, z. B. das Suchen oder Festlegen des Standarddruckers. Weitere Beispiele finden Sie im TechNet ScriptCenter unter https://www.microsoft.com/technet .
ms.assetid: 56aa8043-08cc-42c9-82b0-f1328cd52ff8
ms.tgt_platform: multiple
title: 'WMI-Aufgaben: Drucker und Drucken'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6e580b299e32e2c003c084fb771a28e5984f7e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625576"
---
# <a name="wmi-tasks-printers-and-printing"></a>WMI-Aufgaben: Drucker und Drucken

WMI-Aufgaben für Drucker und Drucken verwalten und erhalten Daten zu Druckern, z. B. das Suchen oder Festlegen des Standarddruckers. Weitere Beispiele finden Sie im TechNet ScriptCenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Die in diesem Thema gezeigten Skriptbeispiele beziehen nur Daten vom lokalen Computer. Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remotecomputern finden Sie unter Herstellen einer Verbindung [mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)


Im folgenden Verfahren wird das Ausführen eines Skripts beschrieben.

**So führen Sie ein Skript aus**

1.  Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung VBS, z. *B.filename.vbs*. Stellen Sie sicher, dass Ihr Text-Editor der .txt datei keine Erweiterung hinzufüge.
2.  Öffnen Sie ein Eingabeaufforderungsfenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.
3.  Geben **Sie cscript filename.vbs** eingabeaufforderung ein.
4.  Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie über eine Eingabeaufforderung mit erhöhten Rechten ausführen. Einige Ereignisprotokollen, z. B. das Sicherheitsereignisprotokoll, können durch Benutzerzugriffssteuerungen (User Access Controls, UAC) geschützt werden.

> [!Note]  
> Standardmäßig zeigt cscript die Ausgabe eines Skripts im Eingabeaufforderungsfenster an. Da WMI-Skripts große Mengen an Ausgabe erzeugen können, sollten Sie die Ausgabe an eine Datei umleiten. Geben **Sie cscript filename.vbs > outfile.txt** eingabeaufforderung ein, um  die Ausgabe des skriptsfilename.vbsan *outfile.txt.*

 

In der folgenden Tabelle sind Skriptbeispiele aufgeführt, die zum Abrufen verschiedener Datentypen vom lokalen Computer verwendet werden können.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Vorgehensweisen</th>
<th>WMI-Klassen oder -Methoden</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... Eine neue Druckerverbindung zu einem Remotecomputer hinzufügen?</td>
<td>Verwenden Sie <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/addprinterconnection-method-in-class-win32-printer"><strong>AddPrinterConnection-Methode.</strong></a><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-ws-01&quot;
Set objWMIService = GetObject( &quot;winmgmts:{impersonationLevel=Impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objPrinter = objWMIService.Get(&quot;Win32_Printer&quot;)
errReturn = objPrinter.AddPrinterConnection (&quot;\\PrintServer1\ArtDepartmentPrinter&quot;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... Standarddrucker festlegen?</td>
<td><p>Verwenden Sie <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/setdefaultprinter-method-in-class-win32-printer"><strong>SetDefaultPrinter-Methode.</strong></a></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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
Set colInstalledPrinters =  objWMIService.ExecQuery (&quot;Select * from Win32_Printer Where Name = &#39;ScriptedPrinter&#39;&quot;)
For Each objPrinter in colInstalledPrinters
    objPrinter.SetDefaultPrinter()
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$printerName = &quot;\\ServerName\ShareName&quot;
$printer = get-wmiObject -class win32_printer -Namespace $namespace | Where-Object { $_.Name -eq $printerName }
[void]$printer.setDefaultPrinter()</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... Druckaufträge mit WMI abbrechen?</td>
<td><p>Verwenden Sie <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/cancelalljobs-method-in-class-win32-printer"><strong>CancelAllJobs-Methode.</strong></a></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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
Set colPrintJobs =  objWMIService.ExecQuery (&quot;Select * from Win32_Printer&quot;)
For Each objPrintJob in colPrintJobs 
    objPrintJob.CancelAllJobs
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$result = (get-wmiObject -class win32_printer -Namespace &quot;root\cimv2&quot;).CancelAllJobs()</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... Den Standarddrucker für einen Computer ermitteln?</td>
<td><p>Verwenden <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong></strong></a> Sie die Win32_Printer-Klasse, und überprüfen Sie, ob <strong>die Default-Eigenschaft</strong> <strong>true ist.</strong></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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
Set colInstalledPrinters =  objWMIService.ExecQuery (&quot;Select * from Win32_Printer Where Default = True&quot;)
For Each objPrinter in colInstalledPrinters
    Wscript.Echo objPrinter.Name
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>get-wmiObject -class win32_printer -Namespace &quot;root\cimv2&quot; | where-object { $_.Default -eq &#39;True&#39; }</code></pre></td>
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

 

