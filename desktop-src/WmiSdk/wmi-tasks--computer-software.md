---
description: WMI-Tasks für Computersoftware erhalten Informationen wie z. b. die Software, die von der Microsoft Windows Installer (MSI) und den Softwareversionen installiert wird. Weitere Beispiele finden Sie im technet scriptcenter unter https://www.microsoft.com/technet .
ms.assetid: 65a61be3-7870-4178-9e96-78b82898271f
ms.tgt_platform: multiple
title: 'WMI-Tasks: Computer Software'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 800a42764cbb1b9552a8ecc87debc04685d28850
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530074"
---
# <a name="wmi-tasks-computer-software"></a><span data-ttu-id="f8e5c-104">WMI-Tasks: Computer Software</span><span class="sxs-lookup"><span data-stu-id="f8e5c-104">WMI Tasks: Computer Software</span></span>

<span data-ttu-id="f8e5c-105">WMI-Tasks für Computersoftware erhalten Informationen wie z. b. die Software, die von der Microsoft Windows Installer (MSI) und den Softwareversionen installiert wird.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-105">WMI tasks for computer software obtain information such as which software is installed by the Microsoft Windows Installer (MSI) and software versions.</span></span> <span data-ttu-id="f8e5c-106">Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f8e5c-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="f8e5c-107">In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="f8e5c-108">Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="f8e5c-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="f8e5c-109">Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="f8e5c-110">**So führen Sie ein Skript aus**</span><span class="sxs-lookup"><span data-stu-id="f8e5c-110">**To run a script**</span></span>

1.  <span data-ttu-id="f8e5c-111">Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="f8e5c-112">Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="f8e5c-113">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="f8e5c-114">Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="f8e5c-115">Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="f8e5c-116">Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="f8e5c-117">Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="f8e5c-118">Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="f8e5c-119">Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

> [!Note]  
> <span data-ttu-id="f8e5c-120">Das Ausführen einer \* Abfrage vom Typ "Select from Win32 \_ Product" kann zu unerwartetem Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-120">Running a "Select \* from Win32\_Product" query may result in unexpected behavior.</span></span> <span data-ttu-id="f8e5c-121">Dies liegt daran, dass der Anbieter, der Win32-Produkte unterstützt, \_ nicht Abfrage optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-121">This is because the provider that supports Win32\_Product is not query optimized.</span></span> <span data-ttu-id="f8e5c-122">Weitere Informationen finden Sie im [KB-Artikel 974524](https://support.microsoft.com/kb/974524).</span><span class="sxs-lookup"><span data-stu-id="f8e5c-122">For more information, see [KB Article 974524](https://support.microsoft.com/kb/974524).</span></span>

 

<span data-ttu-id="f8e5c-123">In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-123">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8e5c-124">Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="f8e5c-124">How do I...</span></span></th>
<th><span data-ttu-id="f8e5c-125">WMI-Klassen oder-Methoden</span><span class="sxs-lookup"><span data-stu-id="f8e5c-125">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f8e5c-126">... Software mithilfe eines Skripts deinstallieren?</span><span class="sxs-lookup"><span data-stu-id="f8e5c-126">...uninstall software using a script?</span></span></td>
<td><span data-ttu-id="f8e5c-127">Wenn die Software mithilfe von Microsoft Windows Installer (MSI) installiert wurde, verwenden Sie die WMI-Klasse <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> und die <a href="/previous-versions/windows/desktop/msiprov/uninstall-method-in-class-win32-product"><strong>Deinstallations</strong></a> Methode.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-127">If the software was installed using Microsoft Windows Installer (MSI), use the WMI class <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> and the <a href="/previous-versions/windows/desktop/msiprov/uninstall-method-in-class-win32-product"><strong>Uninstall</strong></a> method.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8e5c-128">VB</span><span class="sxs-lookup"><span data-stu-id="f8e5c-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Product &quot; _
        & &quot;Where Name = &#39;Personnel database&#39;&quot;)
For Each objSoftware in colSoftware
    objSoftware.Uninstall()
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
<th><span data-ttu-id="f8e5c-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f8e5c-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product | Where-Object {$_.name -eq &quot;Personnel database&quot;}

foreach ($colItem in $colSoftware)
{
    $colItem.Uninstall()
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8e5c-130">... Inventarisieren Sie sämtliche auf einem Computer installierte Software mit einem Skript?</span><span class="sxs-lookup"><span data-stu-id="f8e5c-130">...inventory all the software installed on a computer with a script?</span></span></td>
<td><p><span data-ttu-id="f8e5c-131">Wenn die Software mit Microsoft Windows Installer (MSI) installiert wurde, verwenden Sie die WMI-Klasse <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-131">If the software was installed using Microsoft Windows Installer (MSI) use the WMI class <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8e5c-132">VB</span><span class="sxs-lookup"><span data-stu-id="f8e5c-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Product&quot;)

For Each objSoftware in colSoftware
    Wscript.Echo &quot;Name: &quot; & objSoftware.Name
    Wscript.Echo &quot;Version: &quot; & objSoftware.Version
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
<th><span data-ttu-id="f8e5c-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f8e5c-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product

foreach ($colItem in $colSoftware)
{
    &quot;Name: &quot; + $colItem.Name
    &quot;Version: &quot;+ $colItem.Version
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8e5c-134">... Legen Sie fest, welche Version von Microsoft Office installiert ist?</span><span class="sxs-lookup"><span data-stu-id="f8e5c-134">...determine what version of Microsoft Office is installed?</span></span></td>
<td><p><span data-ttu-id="f8e5c-135">Verwenden Sie die <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> -Klasse, und überprüfen Sie den Wert der Eigenschaft <strong>Version</strong> .</span><span class="sxs-lookup"><span data-stu-id="f8e5c-135">Use the <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> class and check the value of the <strong>Version</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f8e5c-136">VB</span><span class="sxs-lookup"><span data-stu-id="f8e5c-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery(_
    &quot;Select * from Win32_Product &quot; & _
    &quot;Where IdentifyingNumber =&quot; _
        & &quot; &#39;{90280409-6000-11D3-8CFE-0050048383C9}&#39;&quot;)
For Each objItem in colSoftware
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;Version: &quot; & objItem.Version
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
<th><span data-ttu-id="f8e5c-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f8e5c-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product | Where-Object {$_.IdentifyingNumber -eq &quot;{90280409-6000-11D3-8CFE-0050048383C9}&quot;}

foreach ($colItem in $colSoftware)
{
    &quot;Name: &quot; + $colItem.Name
    &quot;Version: &quot; + $colItem.Version
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="f8e5c-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8e5c-138">Examples</span></span>

<span data-ttu-id="f8e5c-139">Das PowerShell-PowerShell-Codebeispiel [PowerShell-Remote-PC-Informations Skript](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) verwendet eine Reihe von Hardware-und Software Klassen, einschließlich Win32Product, um mithilfe von WMI und der Remote Registrierung verschiedene Informationen zu einem Remote Computer zu finden.</span><span class="sxs-lookup"><span data-stu-id="f8e5c-139">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) PowerShell code sample uses a number of hardware and software classes, including Win32Product, to find various information about a remote PC using WMI and the remote registry.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8e5c-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8e5c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8e5c-141">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="f8e5c-141">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="f8e5c-142">WMI C++ Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="f8e5c-142">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="f8e5c-143">Technet scriptcenter</span><span class="sxs-lookup"><span data-stu-id="f8e5c-143">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

