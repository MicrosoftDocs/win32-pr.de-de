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
# <a name="wmi-tasks-registry"></a>WMI-Tasks: Registrierung

WMI-Tasks für die Registrierung erstellen und ändern Registrierungsschlüssel und-Werte. Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

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
<td>... Lesen Sie die Registrierungsschlüssel Werte mithilfe von WMI?</td>
<td>Verwenden Sie die <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> -Klasse im root\DEFAULT-Namespace. Sie können keine Instanzen dieser Klasse erhalten, da der <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">System Registrierungs Anbieter</a> nur eine Methode und einen Ereignis Anbieter ist. Sie können jedoch Registrierungsdaten über Methoden wie z. b. <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> oder <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>enumValue</strong></a>erhalten. Die <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, die sich im root\cimv2-Namespace befindet, ruft Daten über die Registrierung als Ganzes ab, z. b. wie groß Sie ist.<br/> <span data-codelanguage="VisualBasic"></span>
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
<th>PowerShell</th>
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
<td>... neuen Registrierungsschlüssel erstellen?</td>
<td><p>Verwenden Sie die Klasse " <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> ", die sich im root\DEFAULT-Namespace befindet, und die Methode " <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>kreatekey</strong></a> ".</p>
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
<th>PowerShell</th>
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
<td>... einen neuen Registrierungs Wert unter einem Schlüssel erstellen?</td>
<td><p>Verwenden Sie die Klasse " <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> ", die sich im Namespace "root\default" befindet, und die Methode " <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>kreatekey</strong></a> ". Verwenden Sie dann eine der Set-Methoden, je nachdem, welchen Registrierungs Datentyp der Wert ist, z. b. <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>. Die Set-Methoden erstellen einen Wert, wenn er nicht bereits vorhanden ist. Weitere Informationen finden Sie unter <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping eines Registrierungs Datentyps zu einem WMI-Datentyp</a>.</p>
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
<th>PowerShell</th>
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
<td>... vermeiden Sie einen ungültigen Klassen Fehler, wenn Sie versuchen, ein Skript zum Lesen der Registrierung zu schreiben?</td>
<td><p>Verwenden Sie den Namespace root\default, wenn Sie auf die Klasse <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> zugreifen. <strong>StdRegProv</strong> ist nicht Teil des cimv2-Namespace, weshalb ein &quot; Ungültiger Klassen &quot; Fehler generiert wird, wenn Sie versuchen, eine Verbindung mit &quot; root\cimv2: StdRegProv herzustellen &quot; .</p>
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
<td>... Überprüfen Sie die Sicherheit für einen bestimmten Registrierungsschlüssel?</td>
<td><p>Verwenden Sie die Klasse <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , die sich im root\DEFAULT-Namespace und in der <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> -Methode befindet. Sie können nur die Zugriffsrechte für den aktuellen Benutzer überprüfen, auf dem das Skript oder die Anwendung ausgeführt wird. Die Zugriffsrechte für einen anderen angegebenen Benutzer können nicht überprüft werden.</p></td>
</tr>
<tr class="even">
<td>... binäre Registrierungs Werte lesen und schreiben?</td>
<td><p>Verwenden Sie die Klasse <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , die sich im &quot; root\default &quot; -Namespace und in den Methoden <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>GetBinaryValue</strong></a> und <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> befindet. Registrierungs Werte, die im Befehl Regedt32-Hilfsprogramm als Reihe von Byte-hexadezimal Werten angezeigt werden, liegen im <strong>REG_BINARY</strong> Datenformat vor. Weitere Informationen finden Sie unter <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping eines Registrierungs Datentyps zu einem WMI-Datentyp</a>. Im folgenden VBScript-Codebeispiel wird ein neuer Schlüssel mit einem binären Wert erstellt. Der binäre Wert wird im <em>ivalues</em> -Bytearray angegeben, das in HEX angegeben ist.</p>
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
<p>Das folgende Skript liest den Binär Wert.</p>
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
<th>PowerShell</th>
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
<td>... Lesen und Schreiben von Registrierungs Werten, die mehrere Zeichen folgen enthalten?</td>
<td><p>Verwenden Sie die Klasse <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> , die sich im root\DEFAULT-Namespace und in den Methoden <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> und <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> befindet. Registrierungsschlüssel, die im Befehl Regedt32-Hilfsprogramm als eine Reihe von durch Leerzeichen getrennten Zeichen folgen angezeigt werden, liegen im <strong>REG_MULTI_SZ</strong> Datenformat vor. Weitere Informationen finden Sie unter <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping eines Registrierungs Datentyps zu einem WMI-Datentyp</a>. Im folgenden VBScript-Codebeispiel werden ein neuer Schlüssel und ein neuer mehrteilige Zeichen folgen Wert erstellt.</p>
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
<th>PowerShell</th>
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
<p>Das folgende Skript liest den betreffenden-Wert.</p>
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
<th>PowerShell</th>
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
<td>... einen Registrierungsschlüssel entfernen?</td>
<td><p>Verwenden Sie die <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> -Klasse im root\DEFAULT-Namespace und in den <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> -Methoden.</p>
<div class="code">
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



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[WMI C++ Anwendungsbeispiele](wmi-c---application-examples.md)
</dt> <dt>

[Technet scriptcenter](https://www.microsoft.com/technet/scriptcenter)
</dt> <dt>

[Ändern der System Registrierung](modifying-the-system-registry.md)
</dt> <dt>

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)
</dt> </dl>
