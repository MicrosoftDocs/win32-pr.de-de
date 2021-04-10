---
description: WMI-Tasks für die Desktop Verwaltung können die Steuerung und den Abruf von Daten entweder von einem Remote Desktop oder von einem lokalen Computer aus ausführen.
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
ms.openlocfilehash: 33f027c808a30463f2747d11020f45d1b8d40edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864008"
---
# <a name="wmi-tasks-desktop-management"></a><span data-ttu-id="838f4-103">WMI-Tasks: Desktopverwaltung </span><span class="sxs-lookup"><span data-stu-id="838f4-103">WMI Tasks: Desktop Management</span></span>

<span data-ttu-id="838f4-104">WMI-Tasks für die Desktop Verwaltung können die Steuerung und den Abruf von Daten entweder von einem Remote Desktop oder von einem lokalen Computer aus ausführen.</span><span class="sxs-lookup"><span data-stu-id="838f4-104">WMI tasks for desktop management can exert control and obtain data from either a remote desktop or a local computer.</span></span> <span data-ttu-id="838f4-105">Beispielsweise können Sie feststellen, ob für den Bildschirmschoner auf einem lokalen Computer ein Kennwort erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="838f4-105">For example, you can determine whether the screensaver on a local computer requires a password.</span></span> <span data-ttu-id="838f4-106">WMI bietet Ihnen außerdem die Möglichkeit, einen Remote Computer herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="838f4-106">WMI also gives you the ability shut down a remote computer.</span></span> <span data-ttu-id="838f4-107">Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="838f4-107">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="838f4-108">In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="838f4-108">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="838f4-109">Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="838f4-109">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="838f4-110">Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="838f4-110">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="838f4-111">**So führen Sie ein Skript aus**</span><span class="sxs-lookup"><span data-stu-id="838f4-111">**To run a script**</span></span>

1.  <span data-ttu-id="838f4-112">Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="838f4-112">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="838f4-113">Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="838f4-113">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="838f4-114">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="838f4-114">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="838f4-115">Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="838f4-115">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="838f4-116">Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="838f4-116">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="838f4-117">Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.</span><span class="sxs-lookup"><span data-stu-id="838f4-117">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="838f4-118">Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an.</span><span class="sxs-lookup"><span data-stu-id="838f4-118">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="838f4-119">Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="838f4-119">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="838f4-120">Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="838f4-120">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="838f4-121">In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="838f4-121">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-122">Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="838f4-122">How do I...</span></span></th>
<th><span data-ttu-id="838f4-123">WMI-Klassen oder-Methoden</span><span class="sxs-lookup"><span data-stu-id="838f4-123">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="838f4-124">... bestimmen, ob ein Remote Computer im abgesicherten Modus mit Netzwerkstatus gestartet wurde?</span><span class="sxs-lookup"><span data-stu-id="838f4-124">...determine if a remote computer has booted up in the Safe Mode with Networking state?</span></span></td>
<td><span data-ttu-id="838f4-125">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> -Klasse, und überprüfen Sie den Wert der <strong>primaryownername</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="838f4-125">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and check the value of the <strong>PrimaryOwnerName</strong> property.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-126">VB</span><span class="sxs-lookup"><span data-stu-id="838f4-126">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="838f4-127">PowerShell</span></span></th>
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
<td><span data-ttu-id="838f4-128">... bestimmen, ob ein Computerbildschirm Schoner ein Kennwort erfordert?</span><span class="sxs-lookup"><span data-stu-id="838f4-128">...determine if a computer screensaver requires a password?</span></span></td>
<td><p><span data-ttu-id="838f4-129">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-desktop"><strong>Win32_Desktop</strong></a> -Klasse, und überprüfen Sie den Wert der <strong>ScreenSaverSecure</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="838f4-129">Use the <a href="/windows/desktop/CIMWin32Prov/win32-desktop"><strong>Win32_Desktop</strong></a> class and check the value of the <strong>ScreenSaverSecure</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-130">VB</span><span class="sxs-lookup"><span data-stu-id="838f4-130">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="838f4-131">PowerShell</span></span></th>
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
<td><span data-ttu-id="838f4-132">... Überprüfen Sie, ob ein Computerbildschirm 800 Pixel um 600 Pixel festgelegt wurde?</span><span class="sxs-lookup"><span data-stu-id="838f4-132">...verify that a computer screen has been set for 800 pixels by 600 pixels?</span></span></td>
<td><p><span data-ttu-id="838f4-133">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-desktopmonitor"><strong>Win32_DesktopMonitor</strong></a> -Klasse, und überprüfen Sie die Werte der Eigenschaften <strong>ScreenHeight</strong> und <strong>ScreenWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="838f4-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-desktopmonitor"><strong>Win32_DesktopMonitor</strong></a> class and check the values of the properties <strong>ScreenHeight</strong> and <strong>ScreenWidth</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-134">VB</span><span class="sxs-lookup"><span data-stu-id="838f4-134">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="838f4-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><# Get desktop information #>
$computer = &quot;.&quot;
$desktops = Get-WmiObject -Class Win32_DesktopMonitor
$hostname = hostname

<span data-ttu-id="838f4-136">< # anzeigen der Desktop Details # > &quot; es sind {0} Desktops {1} wie folgt: &quot; -f $Desktops. Anzahl, $Hostname &quot; &quot; $i = 1 # Anzahl der Desktops auf diesem System</span><span class="sxs-lookup"><span data-stu-id="838f4-136"><# Display desktop details #> &quot;There are {0} Desktops on {1} as follows:&quot; -f $desktops.Count, $hostname &quot;&quot; $i=1 # count of desktops on this system</span></span>

<span data-ttu-id="838f4-137">foreach ($Desktop in $Desktops) { &quot; Desktop {0} : {1} &quot; -f $i + +, $Desktop. Caption &quot; Screen height: {0} &quot; -f $Desktop. Bildschirmbreite des ScreenHeight &quot; : {0} &quot; -f $Desktop. ScreenWidth &quot; &quot; }</code></span><span class="sxs-lookup"><span data-stu-id="838f4-137">foreach ($desktop in $desktops) { &quot;Desktop {0}: {1}&quot; -f  $i++, $Desktop.Caption &quot;Screen Height : {0}&quot; -f $desktop.ScreenHeight &quot;Screen Width  : {0}&quot; -f $desktop.ScreenWidth &quot;&quot; }</code></span></span></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="838f4-138">... Legen Sie fest, wie lange ein Computer ausgeführt wurde?</span><span class="sxs-lookup"><span data-stu-id="838f4-138">...determine how long a computer has been running?</span></span></td>
<td><p><span data-ttu-id="838f4-139">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> -Klasse und die <strong>LastBootUpTime</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="838f4-139">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <strong>LastBootUpTime</strong> property.</span></span> <span data-ttu-id="838f4-140">Subtrahieren Sie diesen Wert von der aktuellen Zeit, um die Betriebszeit des Systems zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="838f4-140">Subtract that value from the current time to get the system uptime.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-141">VB</span><span class="sxs-lookup"><span data-stu-id="838f4-141">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="838f4-142">PowerShell</span></span></th>
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
<td><span data-ttu-id="838f4-143">... einen Remote Computer neu starten oder Herunterfahren?</span><span class="sxs-lookup"><span data-stu-id="838f4-143">...reboot or shut down a remote computer?</span></span></td>
<td><p><span data-ttu-id="838f4-144">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/win32shutdown-method-in-class-win32-operatingsystem"><strong>Win32Shutdown</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="838f4-144">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/win32shutdown-method-in-class-win32-operatingsystem"><strong>Win32Shutdown</strong></a> method.</span></span> <span data-ttu-id="838f4-145">Beim Herstellen einer Verbindung mit WMI müssen Sie die <a href="privilege-constants.md">RemoteShutdown</a> -Berechtigung einschließen.</span><span class="sxs-lookup"><span data-stu-id="838f4-145">You must include the <a href="privilege-constants.md">RemoteShutdown</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="838f4-146">Weitere Informationen finden Sie unter <a href="executing-privileged-operations-using-vbscript.md">Ausführen von privilegierten Vorgängen mit VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="838f4-146">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span> <span data-ttu-id="838f4-147">Anders als bei der <a href="/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem"><strong>Shutdown</strong></a> -Methode auf <strong>Win32_OperatingSystem</strong>können Sie mithilfe der <strong>Win32Shutdown</strong> -Methode Flags festlegen, um das Verhalten beim Herunterfahren zu steuern.</span><span class="sxs-lookup"><span data-stu-id="838f4-147">Unlike the <a href="/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem"><strong>Shutdown</strong></a> method on <strong>Win32_OperatingSystem</strong>, the <strong>Win32Shutdown</strong> method allows you to set flags to control the shutdown behavior.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-148">VB</span><span class="sxs-lookup"><span data-stu-id="838f4-148">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="838f4-149">PowerShell</span></span></th>
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
<td><span data-ttu-id="838f4-150">... bestimmen, welche Anwendungen automatisch bei jedem Start von Windows ausgeführt werden?</span><span class="sxs-lookup"><span data-stu-id="838f4-150">...determine what applications automatically run each time I start Windows?</span></span></td>
<td><p><span data-ttu-id="838f4-151">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-startupcommand"><strong>Win32_StartupCommand</strong></a> -Klasse.</span><span class="sxs-lookup"><span data-stu-id="838f4-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-startupcommand"><strong>Win32_StartupCommand</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-152">VB</span><span class="sxs-lookup"><span data-stu-id="838f4-152">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="838f4-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="838f4-153">PowerShell</span></span></th>
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



 

## <a name="related-topics"></a><span data-ttu-id="838f4-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="838f4-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="838f4-155">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="838f4-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="838f4-156">WMI C++ Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="838f4-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="838f4-157">Technet scriptcenter</span><span class="sxs-lookup"><span data-stu-id="838f4-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

