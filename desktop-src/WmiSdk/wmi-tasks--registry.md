---
description: WMI-Tasks für die Registrierung erstellen und ändern Registrierungsschlüssel und-Werte. Weitere Beispiele finden Sie im technet scriptcenter unter https://www.microsoft.com/technet .
ms.assetid: 0785189e-9638-4776-8414-1414d7b02524
ms.tgt_platform: multiple
title: 'WMI-Tasks: Registrierung'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df6ae73d41c9cbfd6cd303b72e1b9207f3191c85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369759"
---
# <a name="wmi-tasks-registry"></a><span data-ttu-id="2bcdf-104">WMI-Tasks: Registrierung</span><span class="sxs-lookup"><span data-stu-id="2bcdf-104">WMI Tasks: Registry</span></span>

<span data-ttu-id="2bcdf-105">WMI-Tasks für die Registrierung erstellen und ändern Registrierungsschlüssel und-Werte.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-105">WMI tasks for the registry create and modify registry keys and values.</span></span> <span data-ttu-id="2bcdf-106">Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2bcdf-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="2bcdf-107">In den in diesem Thema gezeigten Skript Beispielen werden nur Daten vom lokalen Computer abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="2bcdf-108">Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remote Computern finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="2bcdf-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="2bcdf-109">Im folgenden Verfahren wird die Vorgehensweise zum Ausführen eines Skripts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="2bcdf-110">**So führen Sie ein Skript aus**</span><span class="sxs-lookup"><span data-stu-id="2bcdf-110">**To run a script**</span></span>

1.  <span data-ttu-id="2bcdf-111">Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung. vb, z. b. *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="2bcdf-112">Stellen Sie sicher, dass der Text-Editor der Datei keine Erweiterung ". txt" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="2bcdf-113">Öffnen Sie ein Eingabe Aufforderungs Fenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="2bcdf-114">Geben Sie **cscript-filename.vbs** an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="2bcdf-115">Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie von einer Eingabeaufforderung mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="2bcdf-116">Einige Ereignisprotokolle, z. b. das Sicherheits Ereignisprotokoll, werden möglicherweise durch die Benutzer Zugriffs Steuerung (User Access Control, UAC) geschützt.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="2bcdf-117">Cscript zeigt standardmäßig die Ausgabe eines Skripts im Eingabe Aufforderungs Fenster an.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="2bcdf-118">Da WMI-Skripts große Mengen an Ausgaben verursachen können, empfiehlt es sich, die Ausgabe in eine Datei umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="2bcdf-119">Geben Sie an der Eingabeaufforderung **cscript filename.vbs > outfile.txt** ein, um die Ausgabe des *filename.vbs* Skripts in *outfile.txt* umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="2bcdf-120">In der folgenden Tabelle sind Skript Beispiele aufgelistet, die zum Abrufen verschiedener Datentypen auf dem lokalen Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bcdf-121">Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="2bcdf-121">How do I...</span></span></th>
<th><span data-ttu-id="2bcdf-122">WMI-Klassen oder-Methoden</span><span class="sxs-lookup"><span data-stu-id="2bcdf-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2bcdf-123">... Lesen Sie die Registrierungsschlüssel Werte mithilfe von WMI?</span><span class="sxs-lookup"><span data-stu-id="2bcdf-123">...read registry key values using WMI?</span></span></td>
<td><span data-ttu-id="2bcdf-124">Verwenden Sie die <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> -Klasse im root\DEFAULT-Namespace.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-124">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace.</span></span> <span data-ttu-id="2bcdf-125">Sie können keine Instanzen dieser Klasse erhalten, da der <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">System Registrierungs Anbieter</a> nur eine Methode und einen Ereignis Anbieter ist.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-125">You cannot get any instances of this class because the <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">System Registry Provider</a> is a method and event provider only.</span></span> <span data-ttu-id="2bcdf-126">Sie können jedoch Registrierungsdaten über Methoden wie z. b. <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> oder <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>enumValue</strong></a>erhalten.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-126">However, you can get registry data through methods such as <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> or <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>EnumValue</strong></a>.</span></span> <span data-ttu-id="2bcdf-127">Die <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, die sich im root\cimv2-Namespace befindet, ruft Daten über die Registrierung als Ganzes ab, z. b. wie groß Sie ist.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-127">The <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, located in root\cimv2 namespace, gets data about the registry as a whole, such as how large it is.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bcdf-128">VB</span><span class="sxs-lookup"><span data-stu-id="2bcdf-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER,strKeyPath,strValueName,dwValue
WScript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
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
<th><span data-ttu-id="2bcdf-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bcdf-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_CURRENT_USER =2147483649
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key = &quot;Console&quot;
$Value = &quot;HistoryBufferSize&quot;
$results = $reg.GetDWORDValue($HKEY_CURRENT_USER, $Key, $value)
&quot;Current History Buffer Size: {0}&quot; -f $results.uValue</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bcdf-130">... neuen Registrierungsschlüssel erstellen?</span><span class="sxs-lookup"><span data-stu-id="2bcdf-130">...create a new registry key?</span></span></td>
<td><p><span data-ttu-id="2bcdf-131">Verwenden Sie die Klasse " <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> ", die sich im root\DEFAULT-Namespace befindet, und die Methode " <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>kreatekey</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="2bcdf-131">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bcdf-132">VB</span><span class="sxs-lookup"><span data-stu-id="2bcdf-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)

strKeyPath = &quot;SOFTWARE\NewKey&quot;
objReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
WScript.Echo &quot;Created registry key HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
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
<th><span data-ttu-id="2bcdf-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bcdf-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.CreateKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key created&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bcdf-134">... einen neuen Registrierungs Wert unter einem Schlüssel erstellen?</span><span class="sxs-lookup"><span data-stu-id="2bcdf-134">...create a new registry value under a key?</span></span></td>
<td><p><span data-ttu-id="2bcdf-135">Verwenden Sie die Klasse " <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> ", die sich im Namespace "root\default" befindet, und die Methode " <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>kreatekey</strong></a> ".</span><span class="sxs-lookup"><span data-stu-id="2bcdf-135">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in the root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span> <span data-ttu-id="2bcdf-136">Verwenden Sie dann eine der Set-Methoden, je nachdem, welchen Registrierungs Datentyp der Wert ist, z. b. <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-136">Then use one of the Set methods, depending on what registry datatype the value is, such as the <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>.</span></span> <span data-ttu-id="2bcdf-137">Die Set-Methoden erstellen einen Wert, wenn er nicht bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-137">The Set methods create a value if it does not already exist.</span></span> <span data-ttu-id="2bcdf-138">Weitere Informationen finden Sie unter <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping eines Registrierungs Datentyps zu einem WMI-Datentyp</a>.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-138">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bcdf-139">VB</span><span class="sxs-lookup"><span data-stu-id="2bcdf-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strValueName = &quot;Example_Expanded_String_Value&quot;
strValue = &quot;%PATHEXT%&quot;
objReg.SetExpandedStringValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,strValue
WScript.Echo &quot;Example expanded_String_Value at &quot; & &quot;HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
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
<th><span data-ttu-id="2bcdf-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bcdf-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example_Expanded_String_Value&quot;
$Value     = &quot;%PATHEXT%&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetExpandedStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Value)
If ($results.Returnvalue -eq 0) {&quot;Value created&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bcdf-141">... vermeiden Sie einen ungültigen Klassen Fehler, wenn Sie versuchen, ein Skript zum Lesen der Registrierung zu schreiben?</span><span class="sxs-lookup"><span data-stu-id="2bcdf-141">...avoid getting an Invalid Class error when trying to write a script to read the registry?</span></span></td>
<td><p><span data-ttu-id="2bcdf-142">Verwenden Sie den Namespace root\default, wenn Sie auf die Klasse <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-142">Use the root\default namespace when accessing the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class.</span></span> <span data-ttu-id="2bcdf-143"><strong>StdRegProv</strong> ist nicht Teil des cimv2-Namespace, weshalb ein &quot; Ungültiger Klassen &quot; Fehler generiert wird, wenn Sie versuchen, eine Verbindung mit &quot; root\cimv2: StdRegProv herzustellen &quot; .</span><span class="sxs-lookup"><span data-stu-id="2bcdf-143"><strong>StdRegProv</strong> is not part of the cimv2 namespace, which is why an &quot;Invalid Class&quot; error is generated if you try to connect to &quot;root\cimv2:StdRegProv&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bcdf-144">VB</span><span class="sxs-lookup"><span data-stu-id="2bcdf-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;) 
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER, strKeyPath, strValueName, dwValue
Wscript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bcdf-145">... Überprüfen Sie die Sicherheit für einen bestimmten Registrierungsschlüssel?</span><span class="sxs-lookup"><span data-stu-id="2bcdf-145">...check security on a specific registry key?</span></span></td>
<td><p><span data-ttu-id="2bcdf-146">Verwenden Sie die Klasse <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , die sich im root\DEFAULT-Namespace und in der <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> -Methode befindet.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-146">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> method.</span></span> <span data-ttu-id="2bcdf-147">Sie können nur die Zugriffsrechte für den aktuellen Benutzer überprüfen, auf dem das Skript oder die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-147">You can only check the access rights for the current user that is running the script or application.</span></span> <span data-ttu-id="2bcdf-148">Die Zugriffsrechte für einen anderen angegebenen Benutzer können nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-148">You cannot check the access rights for another specified user.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bcdf-149">... binäre Registrierungs Werte lesen und schreiben?</span><span class="sxs-lookup"><span data-stu-id="2bcdf-149">...read and write binary registry values?</span></span></td>
<td><p><span data-ttu-id="2bcdf-150">Verwenden Sie die Klasse <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , die sich im &quot; root\default &quot; -Namespace und in den Methoden <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>GetBinaryValue</strong></a> und <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> befindet.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-150">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in &quot;Root\Default&quot; namespace and the <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>GetBinaryValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> methods.</span></span> <span data-ttu-id="2bcdf-151">Registrierungs Werte, die im Befehl Regedt32-Hilfsprogramm als Reihe von Byte-hexadezimal Werten angezeigt werden, liegen im <strong>REG_BINARY</strong> Datenformat vor.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-151">Registry values that appear in the RegEdt32 utility as a series of byte hexadecimal values are in the <strong>REG_BINARY</strong> data format.</span></span> <span data-ttu-id="2bcdf-152">Weitere Informationen finden Sie unter <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping eines Registrierungs Datentyps zu einem WMI-Datentyp</a>.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-152">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="2bcdf-153">Im folgenden VBScript-Codebeispiel wird ein neuer Schlüssel mit einem binären Wert erstellt.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-153">The following VBScript code example creates a new key with a binary value.</span></span> <span data-ttu-id="2bcdf-154">Der binäre Wert wird im <em>ivalues</em> -Bytearray angegeben, das in HEX angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-154">The binary value is supplied in the <em>iValues</em> byte array specified in Hex.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bcdf-155">VB</span><span class="sxs-lookup"><span data-stu-id="2bcdf-155">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&H01,&Ha2,&H10)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
strKeyPath = &quot;SOFTWARE\NewKey&quot;
BinaryValueName = &quot;Example Binary Value&quot;

oReg.SetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,BinaryValueName,iValues</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="2bcdf-156">Das folgende Skript liest den Binär Wert.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-156">The following script reads the binary value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bcdf-157">VB</span><span class="sxs-lookup"><span data-stu-id="2bcdf-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002 
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strValueName = &quot;Example Binary Value&quot;
strComputer = &quot;.&quot;
dim iValues(3)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.GetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,iValues
For i = lBound(iValues) to uBound(iValues)
Wscript.Echo iValues(i)
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
<th><span data-ttu-id="2bcdf-158">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bcdf-158">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example Binary Value&quot;
$Values     = @(0x54, 0x46, 0x4C)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.GetBinaryValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
Foreach ($byte in $results.uvalue) {&quot;{0}&quot; -f $byte.tostring(&quot;x&quot;)}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2bcdf-159">... Lesen und Schreiben von Registrierungs Werten, die mehrere Zeichen folgen enthalten?</span><span class="sxs-lookup"><span data-stu-id="2bcdf-159">...read and write registry values that contain multiple strings?</span></span></td>
<td><p><span data-ttu-id="2bcdf-160">Verwenden Sie die Klasse <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , die sich im root\DEFAULT-Namespace und in den Methoden <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> und <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> befindet.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-160">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> methods.</span></span> <span data-ttu-id="2bcdf-161">Registrierungsschlüssel, die im Befehl Regedt32-Hilfsprogramm als eine Reihe von durch Leerzeichen getrennten Zeichen folgen angezeigt werden, liegen im <strong>REG_MULTI_SZ</strong> Datenformat vor.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-161">Registry keys that appear in the RegEdt32 utility as a series of strings separated by spaces are in the <strong>REG_MULTI_SZ</strong> data format.</span></span> <span data-ttu-id="2bcdf-162">Weitere Informationen finden Sie unter <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping eines Registrierungs Datentyps zu einem WMI-Datentyp</a>.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-162">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="2bcdf-163">Im folgenden VBScript-Codebeispiel werden ein neuer Schlüssel und ein neuer mehrteilige Zeichen folgen Wert erstellt.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-163">The following VBScript code example creates a new key and a new multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bcdf-164">VB</span><span class="sxs-lookup"><span data-stu-id="2bcdf-164">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
MultValueName = &quot;Example Multistring Value&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
oReg.SetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues</code></pre></td>
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
<th><span data-ttu-id="2bcdf-165">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bcdf-165">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$Values     = @(&quot;Thomas&quot;, &quot;Susan&quot;, &quot;Rebecca&quot;)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Values)
If ($results.Returnvalue -eq 0) {&quot;Value Set&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="2bcdf-166">Das folgende Skript liest den betreffenden-Wert.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-166">The following script reads the multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bcdf-167">VB</span><span class="sxs-lookup"><span data-stu-id="2bcdf-167">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
MultValueName = &quot;Example Multistring Value&quot;
oReg.GetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues
For Each strValue In iValues
WScript.echo strValue
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
<th><span data-ttu-id="2bcdf-168">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bcdf-168">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Define Constants
$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$results   = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
$results.svalue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2bcdf-169">... einen Registrierungsschlüssel entfernen?</span><span class="sxs-lookup"><span data-stu-id="2bcdf-169">...remove a registry key?</span></span></td>
<td><p><span data-ttu-id="2bcdf-170">Verwenden Sie die <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> -Klasse im root\DEFAULT-Namespace und in den <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> -Methoden.</span><span class="sxs-lookup"><span data-stu-id="2bcdf-170">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> methods.</span></span></p>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2bcdf-171">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2bcdf-171">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.DeleteKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key Removed&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2bcdf-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2bcdf-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bcdf-173">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="2bcdf-173">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="2bcdf-174">WMI C++ Anwendungsbeispiele</span><span class="sxs-lookup"><span data-stu-id="2bcdf-174">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="2bcdf-175">Technet scriptcenter</span><span class="sxs-lookup"><span data-stu-id="2bcdf-175">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> <dt>

[<span data-ttu-id="2bcdf-176">Ändern der System Registrierung</span><span class="sxs-lookup"><span data-stu-id="2bcdf-176">Modifying the System Registry</span></span>](modifying-the-system-registry.md)
</dt> <dt>

[<span data-ttu-id="2bcdf-177">**StdRegProv**</span><span class="sxs-lookup"><span data-stu-id="2bcdf-177">**StdRegProv**</span></span>](/previous-versions/windows/desktop/regprov/stdregprov)
</dt> </dl>
