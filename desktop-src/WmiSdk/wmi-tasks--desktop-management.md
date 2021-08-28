---
description: WMI-Aufgaben für die Desktopverwaltung können die Steuerung steuern und Daten von einem Remotedesktop oder einem lokalen Computer abrufen.
ms.assetid: bb8356bf-de38-4925-a501-6ad47d23ea8f
ms.tgt_platform: multiple
title: 'WMI-Tasks: Desktopverwaltung '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 25d5af34a252243610a639bc89ed2a7a522775fa
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623356"
---
# <a name="wmi-tasks-desktop-management"></a>WMI-Tasks: Desktopverwaltung 

WMI-Aufgaben für die Desktopverwaltung können die Steuerung steuern und Daten von einem Remotedesktop oder einem lokalen Computer abrufen. Beispielsweise können Sie bestimmen, ob der Bildschirmschoner auf einem lokalen Computer ein Kennwort erfordert. WMI bietet Ihnen auch die Möglichkeit, einen Remotecomputer herunterzufahren. Weitere Beispiele finden Sie im TechNet ScriptCenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Die in diesem Thema gezeigten Skriptbeispiele rufen Daten nur vom lokalen Computer ab. Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remotecomputern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)


Im folgenden Verfahren wird beschrieben, wie Ein Skript ausgeführt wird.

**So führen Sie ein Skript aus**

1.  Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung .vbs, z. *B.filename.vbs*. Stellen Sie sicher, dass Ihr Text-Editor der Datei keine .txt Erweiterung hinzufüg.
2.  Öffnen Sie ein Eingabeaufforderungsfenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.
3.  Geben Sie an der Eingabeaufforderung **cscript filename.vbs** ein.
4.  Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie über eine Eingabeaufforderung mit erhöhten Rechten ausführen. Einige Ereignisprotokolle, z. B. das Sicherheitsereignisprotokoll, können durch Benutzerzugriffssteuerungen (User Access Controls, UAC) geschützt werden.

> [!Note]  
> Standardmäßig zeigt cscript die Ausgabe eines Skripts im Eingabeaufforderungsfenster an. Da WMI-Skripts große Mengen von Ausgaben erzeugen können, sollten Sie die Ausgabe an eine Datei umleiten. Geben Sie **cscript filename.vbs > outfile.txt** an der Eingabeaufforderung ein, um die Ausgabe des *filename.vbs* Skripts anoutfile.txt *umzuleiten.*

 

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
<td>... Ermitteln Sie, ob ein Remotecomputer im Tresor-Modus mit dem Status Netzwerk gestartet wurde?</td>
<td>Verwenden <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong></strong></a> Sie die Win32_ComputerSystem-Klasse, und überprüfen Sie den Wert der <strong>PrimaryOwnerName-Eigenschaft.</strong><br/> <span data-codelanguage="VisualBasic"></span>
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
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery (&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Registered owner: &quot; & objComputer.PrimaryOwnerName
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
<td><pre><code>$colSettings = Get-WmiObject -Class Win32_ComputerSystem
foreach ($objComputer in $colSettings)
{
    &quot;System Name: &quot; + $objComputer.Name
    &quot;Registered owner: &quot; + $objComputer.PrimaryOwnerName
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... ermitteln, ob ein Bildschirmschoner für einen Computer ein Kennwort erfordert?</td>
<td><p>Verwenden <a href="/windows/desktop/CIMWin32Prov/win32-desktop"><strong></strong></a> Sie die Win32_Desktop-Klasse, und überprüfen Sie den Wert der <strong>ScreenSaverSecure-Eigenschaft.</strong></p>
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
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_Desktop&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Screen Saver Secure: &quot; & objItem.ScreenSaverSecure
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
<td><pre><code>$Computer = &quot;.&quot;
$Desktops = Get-WMIObject -class Win32_Desktop -ComputerName $computer
&quot;{0} desktops found as follows&quot; -f $desktops.count
foreach ($desktop in $desktops) {
     &quot;Desktop      : {0}&quot;  -f $Desktop.Name
     &quot;Screen Saver : {0}&quot;  -f $desktop.ScreensaverExecutable
     &quot;Secure       : {0} &quot; -f $desktop.ScreenSaverSecure
     &quot;&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... Überprüfen Sie, ob ein Computerbildschirm auf 800 x 600 Pixel festgelegt wurde?</td>
<td><p>Verwenden <a href="/windows/desktop/CIMWin32Prov/win32-desktopmonitor"><strong></strong></a> Sie die Win32_DesktopMonitor-Klasse, und überprüfen Sie die Werte der Eigenschaften <strong>ScreenHeight</strong> und <strong>ScreenWidth.</strong></p>
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
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_DesktopMonitor&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Screen Height: &quot; & objItem.ScreenHeight
    Wscript.Echo &quot;Screen Width: &quot; & objItem.ScreenWidth
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
<td><pre><code><# Get desktop information #>
$computer = &quot;.&quot;
$desktops = Get-WmiObject -Class Win32_DesktopMonitor
$hostname = hostname

<# Desktopdetails anzeigen #> &quot; Es gibt {0} Desktops auf wie {1} folgt: &quot; -f $desktops. Anzahl, $hostname &quot; &quot; $i=1 Anzahl der Desktops auf diesem System

foreach ($desktop in $desktops) { &quot; Desktop {0} : {1} &quot; -f $i++, $Desktop.Caption Screen &quot; Height : {0} &quot; -f $desktop. &quot;ScreenHeight-Bildschirmbreite: {0} &quot; -f $desktop. ScreenWidth &quot; &quot; }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... bestimmen, wie lange ein Computer ausgeführt wurde?</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem-Klasse</strong></a> und die <strong>LastBootUpTime-Eigenschaft.</strong> Subtrahieren Sie diesen Wert von der aktuellen Zeit, um die Systembetriebszeit zu erhalten.</p>
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
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
 
For Each objOS in colOperatingSystems
    dtmBootup = objOS.LastBootUpTime
    dtmLastBootUpTime = WMIDateStringToDate(dtmBootup)
    dtmSystemUptime = DateDiff(&quot;h&quot;, dtmLastBootUpTime, Now)
    Wscript.Echo dtmSystemUptime 
Next
 
Function WMIDateStringToDate(dtmBootup)
    WMIDateStringToDate =  CDate(Mid(dtmBootup, 5, 2) & &quot;/&quot; & _
        Mid(dtmBootup, 7, 2) & &quot;/&quot; & Left(dtmBootup, 4) & &quot; &quot; & Mid (dtmBootup, 9, 2) & &quot;:&quot; & _
        Mid(dtmBootup, 11, 2) & &quot;:&quot; & Mid(dtmBootup, 13, 2))
End Function</code></pre></td>
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
<td><pre><code>function WMIDateStringToDate($Bootup) {
[System.Management.ManagementDateTimeconverter]::ToDateTime($Bootup)
}

<# Main script #>
$Computer = &quot;.&quot; # adjust as needed
$computers = Get-WMIObject -class Win32_OperatingSystem -computer $computer

foreach ($system in $computers) {
    $Bootup = $system.LastBootUpTime
    $LastBootUpTime = WMIDateStringToDate($Bootup)
    $now = Get-Date
 $Uptime = $now-$lastBootUpTime
    &quot;System Up for: {0}&quot; -f $UpTime
} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... Einen Remotecomputer neu starten oder herunterfahren?</td>
<td><p>Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem-Klasse</strong></a> und die <a href="/windows/desktop/CIMWin32Prov/win32shutdown-method-in-class-win32-operatingsystem"><strong>Win32Shutdown-Methode.</strong></a> Sie müssen die <a href="privilege-constants.md">RemoteShutdown-Berechtigung</a> einschließen, wenn Sie eine Verbindung mit WMI herstellen. Weitere Informationen finden Sie unter <a href="executing-privileged-operations-using-vbscript.md">Ausführen privilegierter Vorgänge mit VBScript.</a> Im Gegensatz zur <a href="/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem"><strong>Shutdown-Methode</strong></a> auf <strong>Win32_OperatingSystem</strong>können Sie mit der <strong>Win32Shutdown-Methode</strong> Flags festlegen, um das Verhalten beim Herunterfahren zu steuern.</p>
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
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Shutdown)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    ObjOperatingSystem.Shutdown(1)
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
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
$colOperatingSystem = Get-WmiObject -Class Win32_OperatingSystem -ComputerName $strComputer -Namespace &quot;wmi\cimv2&quot;
foreach ($objOperatingSystem in $colOperatingSystem)
{
    [void]$objOperatingSystem.Shutdown()
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... bestimmen, welche Anwendungen bei jedem Start Windows automatisch ausgeführt werden?</td>
<td><p>Verwenden <a href="/windows/desktop/CIMWin32Prov/win32-startupcommand"><strong></strong></a> Sie die Win32_StartupCommand-Klasse.</p>
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
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colStartupCommands = objWMIService.ExecQuery _
    (&quot;Select * from Win32_StartupCommand&quot;)
For Each objStartupCommand in colStartupCommands
    Wscript.Echo &quot;Command: &quot; & objStartupCommand.Command & VBNewLine _
    & &quot;Description: &quot; & objStartupCommand.Description & VBNewLine _
    & &quot;Location: &quot; & objStartupCommand.Location & VBNewLine _
    & &quot;Name: &quot; & objStartupCommand.Name & VBNewLine _
    & &quot;SettingID: &quot; & objStartupCommand.SettingID & VBNewLine _
    & &quot;User: &quot; & objStartupCommand.User
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
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_StartupCommand -ComputerName $strComputer
foreach ($objStartupCommand in $colItems) 
{ 
    &quot;Command: &quot; + $objStartupCommand.Command
    &quot;Description: &quot; + $objStartupCommand.Description 
    &quot;Location: &quot; + $objStartupCommand.Location 
    &quot;Name: &quot; + $objStartupCommand.Name 
    &quot;SettingID: &quot; + $objStartupCommand.SettingID 
    &quot;User: &quot; + $objStartupCommand.User
}</code></pre></td>
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

