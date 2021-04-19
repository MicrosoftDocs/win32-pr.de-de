---
description: WMI-Tasks für Datenträger und Dateisysteme erhalten Informationen über den Hardware Status des Laufwerks und logische Volumes. Weitere Beispiele finden Sie im technet scriptcenter unter https://www.microsoft.com/technet .
ms.assetid: d310e5e6-3b67-41bc-b5f2-cea33d0a7a2b
ms.tgt_platform: multiple
title: 'WMI-Tasks: Datenträger und Dateisysteme '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0357a91d893120ec1bb72a7c1d54ad4a5e9a0acf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106369346"
---
# <a name="wmi-tasks-disks-and-file-systems"></a><span data-ttu-id="1e61e-104">WMI-Tasks: Datenträger und Dateisysteme </span><span class="sxs-lookup"><span data-stu-id="1e61e-104">WMI Tasks: Disks and File Systems</span></span>

<span data-ttu-id="1e61e-105">WMI-Tasks für Datenträger und Dateisysteme erhalten Informationen über den Hardware Status des Laufwerks und logische Volumes.</span><span class="sxs-lookup"><span data-stu-id="1e61e-105">WMI tasks for disks and file systems obtain information about disk drive hardware state and logical volumes.</span></span> <span data-ttu-id="1e61e-106">Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1e61e-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="1e61e-107">In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e61e-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="1e61e-108">Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="1e61e-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="1e61e-109">Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1e61e-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="1e61e-110">**So führen Sie ein Skript aus**</span><span class="sxs-lookup"><span data-stu-id="1e61e-110">**To run a script**</span></span>

1.  <span data-ttu-id="1e61e-111">Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="1e61e-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="1e61e-112">Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="1e61e-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="1e61e-113">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="1e61e-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="1e61e-114">Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="1e61e-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="1e61e-115">Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e61e-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="1e61e-116">Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.</span><span class="sxs-lookup"><span data-stu-id="1e61e-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="1e61e-117">Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an.</span><span class="sxs-lookup"><span data-stu-id="1e61e-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="1e61e-118">Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="1e61e-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="1e61e-119">Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="1e61e-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="1e61e-120">In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="1e61e-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e61e-121">Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="1e61e-121">How do I...</span></span></th>
<th><span data-ttu-id="1e61e-122">WMI-Klassen oder-Methoden</span><span class="sxs-lookup"><span data-stu-id="1e61e-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e61e-123">... Ermitteln Sie, wie viel Speicherplatz die einzelnen Benutzer zurzeit auf einem Computer verwenden?</span><span class="sxs-lookup"><span data-stu-id="1e61e-123">...find out how much disk space each user is currently using on a computer?</span></span></td>
<td><span data-ttu-id="1e61e-124">Wenn Sie Datenträger Kontingente verwenden, verwenden Sie die <a href="/previous-versions/windows/desktop/wmipdskq/win32-diskquota"><strong>Win32_DiskQuota</strong></a> -Klasse, und rufen Sie die Werte der Eigenschaften <strong>User</strong> und <strong>DiskSpaceUsed</strong> ab.</span><span class="sxs-lookup"><span data-stu-id="1e61e-124">If you are using disk quotas, then use the <a href="/previous-versions/windows/desktop/wmipdskq/win32-diskquota"><strong>Win32_DiskQuota</strong></a> class and retrieve the values of the <strong>User</strong> and <strong>DiskSpaceUsed</strong> properties.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e61e-125">VB</span><span class="sxs-lookup"><span data-stu-id="1e61e-125">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colQuotas = objWMIService.ExecQuery (&quot;Select * from Win32_DiskQuota&quot;)
For each objQuota in colQuotas
    Wscript.Echo &quot;Volume: &quot;& vbTab &  objQuota.QuotaVolume
    Wscript.Echo &quot;User: &quot;& vbTab &  objQuota.User      
    Wscript.Echo &quot;Disk Space Used: &quot; & vbTab &  objQuota.DiskSpaceUsed
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
<th><span data-ttu-id="1e61e-126">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e61e-126">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_DiskQuota -ComputerName $strComputer
foreach ($objQuota in $colItems) 
{ 
    &quot;Volume: &quot; + $objQuota.QuotaVolume
    &quot;User: &quot; + $objQuota.User      
    &quot;Disk Space Used: &quot; + $objQuota.DiskSpaceUsed
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e61e-127">... bestimmen, ob ein Wechsel Laufwerk einem Computer hinzugefügt oder daraus entfernt wurde?</span><span class="sxs-lookup"><span data-stu-id="1e61e-127">...determine when a removable drive has been added to or removed from a computer?</span></span></td>
<td><p><span data-ttu-id="1e61e-128">Verwenden Sie ein Überwachungs Skript, das die <a href="/windows/desktop/CIMWin32Prov/win32-volumechangeevent"><strong>Win32_VolumeChangeEvent</strong></a> -Klasse abfragt.</span><span class="sxs-lookup"><span data-stu-id="1e61e-128">Use a monitoring script that queries the <a href="/windows/desktop/CIMWin32Prov/win32-volumechangeevent"><strong>Win32_VolumeChangeEvent</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e61e-129">VB</span><span class="sxs-lookup"><span data-stu-id="1e61e-129">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colMonitoredEvents = objWMIService. ExecNotificationQuery( &quot;Select * from Win32_VolumeChangeEvent&quot;)
Do
    Set objLatestEvent = colMonitoredEvents.NextEvent
    Wscript.Echo objLatestEvent.DriveName
    Wscript.Echo objLatestEvent.EventType
    Wscript.Echo objLatestEvent.Time_Created
Loop</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e61e-130">... Stellen Sie fest, ob sich eine CD in einem CD-ROM-Laufwerk befindet?</span><span class="sxs-lookup"><span data-stu-id="1e61e-130">...determine if a CD is in a CD-ROM drive?</span></span></td>
<td><p><span data-ttu-id="1e61e-131">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> -Klasse und die <strong>MediaLoaded</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1e61e-131">Use the <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> class and the <strong>MediaLoaded</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e61e-132">VB</span><span class="sxs-lookup"><span data-stu-id="1e61e-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery( &quot;Select * from Win32_CDROMDrive&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Media Loaded: &quot; & objItem.MediaLoaded
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
<th><span data-ttu-id="1e61e-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e61e-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_CDROMDrive -ComputerName $strComputer
foreach ($objItem in $colItems)
{
    &quot;Device ID: &quot; + $objItem.DeviceID
    &quot;MediaLoaded: &quot; + $objItem.MediaLoaded
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e61e-134">... Stellen Sie fest, ob sich ein Datenträger im Diskettenlaufwerk befindet?</span><span class="sxs-lookup"><span data-stu-id="1e61e-134">...determine if a disk is in the floppy drive?</span></span></td>
<td><p><span data-ttu-id="1e61e-135">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> -Klasse, und überprüfen Sie die Eigenschaft <strong>FreeSpace</strong> .</span><span class="sxs-lookup"><span data-stu-id="1e61e-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class and check the <strong>FreeSpace</strong> property.</span></span> <span data-ttu-id="1e61e-136">Wenn der Wert NULL ist, befindet sich kein Datenträger im Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="1e61e-136">If the value is Null, then no disk is in the drive.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e61e-137">VB</span><span class="sxs-lookup"><span data-stu-id="1e61e-137">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery (&quot;Select * From Win32_LogicalDisk Where DeviceID = &#39;A:&#39;&quot;)

For Each objItem in colItems
    intFreeSpace = objItem.FreeSpace
    If IsNull(intFreeSpace) Then
        Wscript.Echo &quot;There is no disk in the floppy drive.&quot;
    Else
        Wscript.Echo &quot;There is a disk in the floppy drive.&quot;
    End If
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
<th><span data-ttu-id="1e61e-138">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e61e-138">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_LogicalDisk -Namespace &quot;root\cimv2&quot; -ComputerName $strComputer | `
    Where-Object { $_.DeviceID -eq &quot;A:&quot; }

foreach ($objItem in $colItems)
{
    $intFreeSpace = $objItem.FreeSpace
    if ($intFreeSpace -eq $null) { &quot;There is no disk in the floppy drive.&quot; }
    else { &quot;There is a disk in the floppy drive.&quot; }
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e61e-139">... unterscheiden Sie zwischen einer Festplatte und einer Wechsel Datenträger?</span><span class="sxs-lookup"><span data-stu-id="1e61e-139">...distinguish between a fixed hard disk and a removable hard disk?</span></span></td>
<td><p><span data-ttu-id="1e61e-140">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> -Klasse, und überprüfen Sie den Wert der <strong>DriveType</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1e61e-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class and check the value of the <strong>DriveType</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e61e-141">VB</span><span class="sxs-lookup"><span data-stu-id="1e61e-141">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery _
    (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot;& vbTab _
        &  objDisk.DeviceID       
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo &quot;No root directory. &quot; & &quot;Drive type could not be &quot; & &quot;determined.&quot;
        Case 2
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Removable drive.&quot;
        Case 3
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Local hard disk.&quot;
        Case 4
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Network disk.&quot;      
        Case 5
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;Compact disk.&quot;      
        Case 6
            Wscript.Echo &quot;DriveType: &quot;& vbTab &  &quot;RAM disk.&quot;   
        Case Else
            Wscript.Echo &quot;Drive type could not be&quot; & &quot; determined.&quot;
    End Select
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
<th><span data-ttu-id="1e61e-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e61e-142">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colDisks = Get-WmiObject -Class Win32_LogicalDisk -ComputerName $strComputer 

foreach ($objDisk in $colDisks)
{
    &quot;DeviceID: &quot; + $objDisk.deviceID
    switch ($objDisk.DriveType)
    {
        &#39;1&#39; { &quot;No root directory. Drive type could not be determined.&quot; }
        &#39;2&#39; { &quot;DriveType: Removable drive.&quot; }
        &#39;3&#39; { &quot;DriveType: Local hard disk.&quot; }
        &#39;4&#39; { &quot;DriveType: Network disk.&quot; }
        &#39;5&#39; { &quot;DriveType: Compact disk.&quot; }
        &#39;6&#39; { &quot;DriveType: RAM disk.&quot; }
        default: { &quot;Drive type could not be determined.&quot; }
    }
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e61e-143">... Legen Sie fest, welches Dateisystem auf einem Laufwerk verwendet wird?</span><span class="sxs-lookup"><span data-stu-id="1e61e-143">...determine what file system is in use on a drive?</span></span></td>
<td><p><span data-ttu-id="1e61e-144">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> -Klasse und die <strong>File System</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1e61e-144">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class and the <strong>FileSystem</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e61e-145">VB</span><span class="sxs-lookup"><span data-stu-id="1e61e-145">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot; & objDisk.DeviceID       
    Wscript.Echo &quot;File System: &quot; & objDisk.FileSystem
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e61e-146">... bestimmen Sie, wie viel freier Speicherplatz auf einem Laufwerk verfügbar ist?</span><span class="sxs-lookup"><span data-stu-id="1e61e-146">...determine how much free space is available on a drive?</span></span></td>
<td><p><span data-ttu-id="1e61e-147">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> -Klasse und die <strong>FreeSpace</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1e61e-147">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class and the <strong>FreeSpace</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e61e-148">VB</span><span class="sxs-lookup"><span data-stu-id="1e61e-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot; & objDisk.DeviceID       
    Wscript.Echo &quot;Free Disk Space: &quot; & objDisk.FreeSpace
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e61e-149">... Festlegen der Größe eines Laufwerks</span><span class="sxs-lookup"><span data-stu-id="1e61e-149">...determine the size of a drive?</span></span></td>
<td><p><span data-ttu-id="1e61e-150">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> -Klasse und die <strong>size</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1e61e-150">Use the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> class, and the <strong>Size</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e61e-151">VB</span><span class="sxs-lookup"><span data-stu-id="1e61e-151">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService.ExecQuery (&quot;Select * from Win32_LogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;DeviceID: &quot; & objDisk.DeviceID       
    Wscript.Echo &quot;Disk Size: &quot; & objDisk.Size
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e61e-152">... erfahren Sie, welche Laufwerke auf einem Computer zugeordnet sind?</span><span class="sxs-lookup"><span data-stu-id="1e61e-152">...find out what drives are mapped on a computer?</span></span></td>
<td><p><span data-ttu-id="1e61e-153">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-mappedlogicaldisk"><strong>Win32_MappedLogicalDisk</strong></a> -Klasse.</span><span class="sxs-lookup"><span data-stu-id="1e61e-153">Use the <a href="/windows/desktop/CIMWin32Prov/win32-mappedlogicaldisk"><strong>Win32_MappedLogicalDisk</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e61e-154">VB</span><span class="sxs-lookup"><span data-stu-id="1e61e-154">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colDisks = objWMIService. ExecQuery(&quot;Select * from Win32_MappedLogicalDisk&quot;)
For Each objDisk in colDisks
    Wscript.Echo &quot;Device ID: &quot; & objDisk.DeviceID
    Wscript.Echo &quot;Name: &quot; & objDisk.Name
    Wscript.Echo &quot;Free Space: &quot; & objDisk.FreeSpace
    Wscript.Echo &quot;Size: &quot; & objDisk.Size
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e61e-155">... wird eine Festplatte zerlegt?</span><span class="sxs-lookup"><span data-stu-id="1e61e-155">...defragment a hard disk?</span></span></td>
<td><p><span data-ttu-id="1e61e-156">Verwenden Sie die <a href="/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)"><strong>Win32_Volume</strong></a> -Klasse und die <a href="/previous-versions/windows/desktop/vdswmi/defrag-method-in-class-win32-volume"><strong>Defrag</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="1e61e-156">Use the <a href="/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)"><strong>Win32_Volume</strong></a> class and the <a href="/previous-versions/windows/desktop/vdswmi/defrag-method-in-class-win32-volume"><strong>Defrag</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e61e-157">VB</span><span class="sxs-lookup"><span data-stu-id="1e61e-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colVolumes = objWMIService.ExecQuery (&quot;Select * from Win32_Volume Where Name = &#39;K:\\&#39;&quot;)
For Each objVolume in colVolumes
     errResult = objVolume.Defrag()
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e61e-158">... erkennen, welcher Laufwerk Buchstabe einer logischen Datenträger Partition zugeordnet ist?</span><span class="sxs-lookup"><span data-stu-id="1e61e-158">...detect which drive letter is associated with a logical disk partition?</span></span></td>
<td><ol>
<li><span data-ttu-id="1e61e-159">Beginnen Sie mit der <a href="/windows/desktop/CIMWin32Prov/win32-diskdrive"><strong>Win32_DiskDrive</strong></a> -Klasse, und Fragen Sie Instanzen <a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition</strong></a> mithilfe der <strong>DeviceID</strong> -Eigenschaft und der <a href="/windows/desktop/CIMWin32Prov/win32-diskdrivetodiskpartition"><strong>Win32_DiskDriveToDiskPartition</strong></a> Association-Klasse ab.</span><span class="sxs-lookup"><span data-stu-id="1e61e-159">Start with the <a href="/windows/desktop/CIMWin32Prov/win32-diskdrive"><strong>Win32_DiskDrive</strong></a> class and query for instances of <a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition</strong></a> using the <strong>DeviceID</strong> property and the <a href="/windows/desktop/CIMWin32Prov/win32-diskdrivetodiskpartition"><strong>Win32_DiskDriveToDiskPartition</strong></a> association class.</span></span> <span data-ttu-id="1e61e-160">Nun verfügen Sie über eine Sammlung der Partitionen auf dem physischen Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="1e61e-160">Now you have a collection of the partitions on the physical drive.</span></span></li>
<li><span data-ttu-id="1e61e-161">Abfragen der <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> , die die Partition darstellt, mithilfe der <a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition. DeviceID</strong></a> -Eigenschaft und der <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisktopartition"><strong>Win32_LogicalDiskToPartition</strong></a> Association-Klasse.</span><span class="sxs-lookup"><span data-stu-id="1e61e-161">Query for the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk</strong></a> that represents the partition using the <a href="/windows/desktop/CIMWin32Prov/win32-diskpartition"><strong>Win32_DiskPartition.DeviceID</strong></a> property and <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisktopartition"><strong>Win32_LogicalDiskToPartition</strong></a> association class.</span></span></li>
<li><span data-ttu-id="1e61e-162">Hiermit wird der Laufwerk Buchstabe aus der <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk.</strong></a>Geräte-ID abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e61e-162">Get the drive letter from the <a href="/windows/desktop/CIMWin32Prov/win32-logicaldisk"><strong>Win32_LogicalDisk.DeviceID</strong></a>.</span></span></li>
</ol>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e61e-163">VB</span><span class="sxs-lookup"><span data-stu-id="1e61e-163">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>ComputerName = &quot;.&quot;
Set wmiServices  = GetObject ( _
    &quot;winmgmts:{impersonationLevel=Impersonate}!//&quot; & ComputerName)
&#39; Get physical disk drive
Set wmiDiskDrives =  wmiServices.ExecQuery ( &quot;SELECT Caption, DeviceID FROM Win32_DiskDrive&quot;)

For Each wmiDiskDrive In wmiDiskDrives
    WScript.Echo &quot;Disk drive Caption: &quot; & wmiDiskDrive.Caption & VbNewLine & &quot;DeviceID: &quot; & &quot; (&quot; & wmiDiskDrive.DeviceID & &quot;)&quot;

&#39;Use the disk drive device id to
&#39; find associated partition
query = &quot;ASSOCIATORS OF {Win32_DiskDrive.DeviceID=&#39;&quot; _
        & wmiDiskDrive.DeviceID & &quot;&#39;} WHERE AssocClass = Win32_DiskDriveToDiskPartition&quot;    
Set wmiDiskPartitions = wmiServices.ExecQuery(query)

For Each wmiDiskPartition In wmiDiskPartitions
    &#39;Use partition device id to find logical disk
    Set wmiLogicalDisks = wmiServices.ExecQuery _
        (&quot;ASSOCIATORS OF {Win32_DiskPartition.DeviceID=&#39;&quot; _
             & wmiDiskPartition.DeviceID & &quot;&#39;} WHERE AssocClass = Win32_LogicalDiskToPartition&quot;)

For Each wmiLogicalDisk In wmiLogicalDisks
    WScript.Echo &quot;Drive letter associated&quot; _
        & &quot; with disk drive = &quot; _ 
        & wmiDiskDrive.Caption _
        & wmiDiskDrive.DeviceID _
        & VbNewLine & &quot; Partition = &quot; _
        & wmiDiskPartition.DeviceID _
        & VbNewLine & &quot; is &quot; _
        & wmiLogicalDisk.DeviceID
    Next
    Next
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="1e61e-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e61e-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e61e-165">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="1e61e-165">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="1e61e-166">WMI C++ Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="1e61e-166">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="1e61e-167">Technet scriptcenter</span><span class="sxs-lookup"><span data-stu-id="1e61e-167">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
