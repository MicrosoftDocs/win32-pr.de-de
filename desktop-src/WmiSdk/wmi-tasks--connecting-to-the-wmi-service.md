---
description: Um Daten aus WMI auf dem lokalen Computer oder einem Remote Computer zu erhalten, müssen Sie eine Verbindung mit dem WMI-Dienst herstellen, indem Sie eine Verbindung mit einem bestimmten Namespace herstellen.
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: 'WMI-Tasks: Herstellen einer Verbindung mit dem WMI-Dienst'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 751c6c0802c30e113f4a2b7ddc646cdf5646b7dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358818"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a>WMI-Tasks: Herstellen einer Verbindung mit dem WMI-Dienst

Um Daten aus WMI auf dem lokalen Computer oder einem Remote Computer zu erhalten, müssen Sie eine Verbindung mit dem WMI-Dienst herstellen, indem Sie eine Verbindung mit einem bestimmten [*Namespace*](gloss-n.md)herstellen. Verwenden Sie in den meisten Fällen entweder die [Kurznamen-monikerverbindung](creating-a-wmi-script.md) oder die [**Locator**](swbemlocator-connectserver.md) -Verbindung. Weitere Beispiele finden Sie im technet scriptcenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Für Remote Verbindungen sind geeignete Einstellungen für die Windows-Firewall und die DCOM erforderlich. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md) und [Herstellen einer Verbindung über die Windows-Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista). Ab Windows Vista kann sich die Benutzerkontensteuerung (User Account Control, UAC) auf den WMI-Zugriff auswirken. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).

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
<td>... Herstellen einer Verbindung mit einem Remote Computer mithilfe von WMI</td>
<td>Geben Sie einen der folgenden als Teil der monikerverbindungszeichenfolge an: <a href="constructing-a-moniker-string.md"></a><br/>
<ul>
<li>Einen NetBIOS-Computernamen, z. b. &quot; ATL-DC-01&quot;</li>
<li>Einen voll qualifizierten Domänen Namen, z. b. &quot; ATL-DC-01.fabrikam.com&quot;</li>
<li>Eine IPv4-Adresse, z. b. &quot; 192.168.1.1&quot;</li>
<li>Ab Windows Vista können Sie eine IPv6-Adresse angeben, wenn auf dem Zielcomputer und dem Computer, von dem aus Sie die Verbindung herstellen, IPv6 ausgeführt wird.<br/></li>
</ul>
Weitere Informationen finden Sie unter <a href="connecting-to-wmi-on-a-remote-computer.md">Herstellen einer Verbindung mit WMI auf einem Remote Computer</a> und <a href="ipv6-and-ipv4-support-in-wmi.md">IPv6-und IPv4-Unterstützung in WMI</a>.<br/> <span data-codelanguage="VisualBasic"></span>
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
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... Führen Sie ein WMI-Skript unter Alternative Anmelde Informationen aus?</td>
<td><p>Verwenden Sie die Methode " <a href="swbemlocator-connectserver.md"><strong>mpbemlocator. ConnectServer</strong></a> " oder " <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWBEMLocator:: ConnectServer</strong></a> " in C++, und schließen Sie den entsprechenden Benutzernamen und das Kennwort ein. Beim Herstellen einer Verbindung mit dem lokalen Computer können die Anmelde Informationen nicht geändert werden. Weitere Informationen finden Sie unter <a href="creating-a-wmi-script.md">Erstellen eines WMI-Skripts</a> und <a href="connecting-to-wmi-on-a-remote-computer.md">Herstellen einer Verbindung mit WMI auf einem Remote Computer</a>.</p>
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
Set objSWbemLocator = CreateObject(&quot;WbemScripting.SWbemLocator&quot;)
Set objSWbemServices = objSWbemLocator.ConnectServer (strComputer, &quot;root\cimv2&quot;, &quot;fabrikam\administrator&quot;, &quot;password&quot;)
Set colProcessList = objSWbemServices.ExecQuery(&quot;Select * From Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<td><pre><code>$StrComputer = &quot;atl-dc-01&quot;
$strCredentials = &quot;FABRIKAM\administrator&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; -credential $strCredentials `
   -Impersonation Impersonate | format-list -Property Name</code></pre></td>
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
</dt> </dl>

 

 



`
