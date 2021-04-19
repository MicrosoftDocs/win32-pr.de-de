---
description: WMI-Tasks für Dateien und Ordner ändern Datei-oder Ordnereigenschaften über WMI, einschließlich der Erstellung einer Freigabe oder dem Umbenennen einer Datei.
ms.assetid: 91281fe1-0461-48da-ac5c-cab7e8e1b285
ms.tgt_platform: multiple
title: 'WMI-Tasks: Dateien und Ordner'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b24d5f7708b88507cd08b73c0b08a83c94f6bb28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357031"
---
# <a name="wmi-tasks-files-and-folders"></a><span data-ttu-id="393cb-103">WMI-Tasks: Dateien und Ordner</span><span class="sxs-lookup"><span data-stu-id="393cb-103">WMI Tasks: Files and Folders</span></span>

<span data-ttu-id="393cb-104">WMI-Tasks für Dateien und Ordner ändern Datei-oder Ordnereigenschaften über WMI, einschließlich der Erstellung einer Freigabe oder dem Umbenennen einer Datei.</span><span class="sxs-lookup"><span data-stu-id="393cb-104">WMI tasks for files and folders change file or folder properties through WMI, including creating a share or renaming a file.</span></span> <span data-ttu-id="393cb-105">Wenn Sie eine Datei kopieren oder eine Datei lesen und schreiben möchten, ist es am einfachsten, Windows Script Host [FileSystemObject](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) anstelle von WMI zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="393cb-105">If you want to copy a file or read and write a file, the easiest way is to use the Windows Script Host [FileSystemObject](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) rather than WMI.</span></span> <span data-ttu-id="393cb-106">Weitere Beispiele finden Sie im Abschnitt " [Dateien und Ordner](/previous-versions/tn-archive/ee176985(v=technet.10)) " von [technet scriptcenter](https://www.microsoft.com/technet/scriptcenter).</span><span class="sxs-lookup"><span data-stu-id="393cb-106">For other examples, see the [Files and Folders](/previous-versions/tn-archive/ee176985(v=technet.10)) section of the [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter).</span></span>

<span data-ttu-id="393cb-107">[**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) ist eine der wenigen [CIM-Klassen](cimclas.md) in WMI, die implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="393cb-107">[**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) is one of the few [CIM classes](cimclas.md) in WMI that is implemented.</span></span> <span data-ttu-id="393cb-108">Vermeiden Sie es, alle Instanzen von **CIM- \_ Datendateien** auf einem Computer aufzulisten oder abzufragen, weil sich die Datenmenge wahrscheinlich auf die Leistung auswirkt oder der Computer nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="393cb-108">Avoid enumerating or querying for all instances of **CIM\_DataFile** on a computer because the volume of data is likely to either affect performance or cause the computer to stop responding.</span></span>

<span data-ttu-id="393cb-109">In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="393cb-109">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="393cb-110">Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="393cb-110">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="393cb-111">Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="393cb-111">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="393cb-112">**So führen Sie ein Skript aus**</span><span class="sxs-lookup"><span data-stu-id="393cb-112">**To run a script**</span></span>

1.  <span data-ttu-id="393cb-113">Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="393cb-113">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="393cb-114">Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="393cb-114">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="393cb-115">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="393cb-115">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="393cb-116">Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="393cb-116">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="393cb-117">Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="393cb-117">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="393cb-118">Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.</span><span class="sxs-lookup"><span data-stu-id="393cb-118">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="393cb-119">Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an.</span><span class="sxs-lookup"><span data-stu-id="393cb-119">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="393cb-120">Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="393cb-120">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="393cb-121">Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="393cb-121">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="393cb-122">In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="393cb-122">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="393cb-123">Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="393cb-123">How do I...</span></span></th>
<th><span data-ttu-id="393cb-124">WMI-Klassen oder-Methoden</span><span class="sxs-lookup"><span data-stu-id="393cb-124">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="393cb-125">... Datei umbenennen, ohne eine Fehlermeldung zu erhalten?</span><span class="sxs-lookup"><span data-stu-id="393cb-125">...rename a file without getting an error message?</span></span></td>
<td><span data-ttu-id="393cb-126">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_Datafile</strong></a> -Klasse.</span><span class="sxs-lookup"><span data-stu-id="393cb-126">Use the <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> class.</span></span> <span data-ttu-id="393cb-127">Stellen Sie sicher, dass Sie den gesamten Pfadnamen übergeben, wenn Sie die <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> -Methode aufrufen, z &quot; . b &quot; .C:\Scripts\Test.txtstatt &quot;Text.txt&quot; .</span><span class="sxs-lookup"><span data-stu-id="393cb-127">Ensure that you pass the entire path name when calling the <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> method, for example, &quot;C:\Scripts\Test.txt&quot; instead of &quot;Text.txt&quot;.</span></span> <span data-ttu-id="393cb-128">Bei PowerShell ist die Verwendung von <strong>CIM_Datafile</strong> möglicherweise ineffizient.</span><span class="sxs-lookup"><span data-stu-id="393cb-128">For PowerShell, using <strong>CIM_DataFile</strong> may be inefficient.</span></span> <span data-ttu-id="393cb-129">Daher können Sie einfach das Rename-Item-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="393cb-129">As such, you may simply use the Rename-Item cmdlet.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="393cb-130">VB</span><span class="sxs-lookup"><span data-stu-id="393cb-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery (&quot;Select * from CIM_DataFile where Name = &quot; & &quot;&#39;c:\\scripts\\toggle_service.vbs&#39;&quot;)
For Each objFile in colFiles
    errResult = objFile.Rename(&quot;c:\scripts\toggle_service.old&quot;)
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
<th><span data-ttu-id="393cb-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="393cb-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>rename-item c:\scripts\toggle_service.vbs toggle_service.old</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="393cb-132">... bestimmen Sie, ob Benutzer über verfügen. Auf dem Computer gespeicherte MP3-Dateien?</span><span class="sxs-lookup"><span data-stu-id="393cb-132">...determine whether users have .MP3 files stored on their computer?</span></span></td>
<td><p><span data-ttu-id="393cb-133">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_Datafile</strong></a> -Klasse, und wählen Sie mithilfe der folgenden <a href="querying-with-wql.md">WQL</a> - <strong>Where</strong> -Klausel Dateien aus: Where Extension = &quot; MP3 &quot; .</span><span class="sxs-lookup"><span data-stu-id="393cb-133">Use the <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> class and select files using the following <a href="querying-with-wql.md">WQL</a> <strong>WHERE</strong> clause: Where Extension = &quot;MP3&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="393cb-134">VB</span><span class="sxs-lookup"><span data-stu-id="393cb-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery(&quot;Select * from CIM_DataFile where Extension = &#39;mp3&#39;&quot;)
For Each objFile in colFiles
    Wscript.Echo &quot;File Name: &quot; & objFile.Name & &quot;.&quot; & objFile.Extension
    Wscript.Echo &quot;Path: &quot; & objFile.Path
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
<th><span data-ttu-id="393cb-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="393cb-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class CIM_DataFile -namespace &quot;root\cimv2&quot; -Filter &quot;Extension = &#39;mp3&#39;&quot; | `
   format-list Name, Extension, Path</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="393cb-136">... Erstellen Sie freigegebene Ordner auf einem Computer?</span><span class="sxs-lookup"><span data-stu-id="393cb-136">...create shared folders on a computer?</span></span></td>
<td><p><span data-ttu-id="393cb-137">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>Create</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="393cb-137">Use the <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>Create</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="393cb-138">VB</span><span class="sxs-lookup"><span data-stu-id="393cb-138">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 25
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objNewShare = objWMIService.Get(&quot;Win32_Share&quot;)
errReturn = objNewShare.Create(&quot;C:\Finance&quot;, &quot;FinanceShare&quot;, FILE_SHARE, MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;)</code></pre></td>
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
<th><span data-ttu-id="393cb-139">PowerShell</span><span class="sxs-lookup"><span data-stu-id="393cb-139">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$FILE_SHARE = 0
$MAXIMUM_CONNECTIONS = 25

$NewDir = new-item C:\Finance -type directory 
$Shares= [WMICLASS]&quot;Win32_Share&quot;
[void]$Shares.Create(&quot;C:\Finance&quot;,&quot;FinanceShare&quot;, $FILE_SHARE, $MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;) </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="393cb-140">... Ordner kopieren?</span><span class="sxs-lookup"><span data-stu-id="393cb-140">...copy a folder?</span></span></td>
<td><p><span data-ttu-id="393cb-141">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="393cb-141">Use the <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> method.</span></span> <span data-ttu-id="393cb-142">Für PowerShell können Sie einfach das Copy-Item-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="393cb-142">For PowerShell, you can simply use the Copy-Item cmdlet.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="393cb-143">VB</span><span class="sxs-lookup"><span data-stu-id="393cb-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery(&quot;Select * from Win32_Directory where Name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy(&quot;D:\Archive&quot;) 
Next </code></pre></td>
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
<th><span data-ttu-id="393cb-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="393cb-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Copy-Item C:\Scripts -Destination D:\Archive -Recurse</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="393cb-145">... einen Ordner verschieben?</span><span class="sxs-lookup"><span data-stu-id="393cb-145">...move a folder?</span></span></td>
<td><p><span data-ttu-id="393cb-146">Verwenden Sie die <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> -Klasse und die <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> -Methode.</span><span class="sxs-lookup"><span data-stu-id="393cb-146">Use the <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> method.</span></span> <span data-ttu-id="393cb-147">Für PowerShell können Sie einfach das Move-Item-Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="393cb-147">For PowerShell, you can simply use the Move-Item cmdlet.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="393cb-148">VB</span><span class="sxs-lookup"><span data-stu-id="393cb-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:&quot; _ 
    & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery _ 
    (&quot;Select * from Win32_Directory where name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename(&quot;C:\Admins\Documents\Archive\VBScript&quot;) 
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
<th><span data-ttu-id="393cb-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="393cb-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>move-item -path C:\Scripts -destination C:\Admins\Documents\Archive\PowerShell</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="393cb-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="393cb-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="393cb-151">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="393cb-151">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="393cb-152">WMI C++ Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="393cb-152">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="393cb-153">Technet scriptcenter</span><span class="sxs-lookup"><span data-stu-id="393cb-153">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
