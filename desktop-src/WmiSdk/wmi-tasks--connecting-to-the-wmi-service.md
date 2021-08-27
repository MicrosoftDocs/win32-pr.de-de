---
description: Um Daten aus WMI entweder auf dem lokalen Computer oder von einem Remotecomputer zu erhalten, müssen Sie eine Verbindung mit dem WMI-Dienst herstellen, indem Sie eine Verbindung mit einem bestimmten Namespace herstellen.
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: 'WMI-Aufgaben: Herstellen einer Verbindung mit dem WMI-Dienst'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da816b45709f6140efb7e6e0460e27d9f9ed00f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627716"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a>WMI-Aufgaben: Herstellen einer Verbindung mit dem WMI-Dienst

Um Daten aus WMI entweder auf dem lokalen Computer oder von einem Remotecomputer zu erhalten, müssen Sie eine Verbindung mit dem WMI-Dienst herstellen, indem Sie eine Verbindung mit einem bestimmten [*Namespace herstellen.*](gloss-n.md) Verwenden Sie in den meisten Fällen entweder die [Kurzzeitmonikerverbindung](creating-a-wmi-script.md) oder die [**Locator-Verbindung.**](swbemlocator-connectserver.md) Weitere Beispiele finden Sie im TechNet ScriptCenter unter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Remoteverbindungen erfordern die richtigen Einstellungen für Windows Firewall und DCOM. Weitere Informationen finden Sie unter Herstellen einer Verbindung mit [WMI auf](connecting-to-wmi-on-a-remote-computer.md) einem Remotecomputer und Herstellen einer Verbindung [über Windows Firewall.](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista) Ab Windows Vista kann sich die Benutzerkontensteuerung (User Account Control, UAC) auf den WMI-Zugriff auswirken. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](user-account-control-and-wmi.md)

Die in diesem Thema gezeigten Skriptbeispiele beziehen nur Daten vom lokalen Computer. Weitere Informationen zur Verwendung des Skripts zum Abrufen von Daten von Remotecomputern finden Sie unter Herstellen einer Verbindung [mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)


Im folgenden Verfahren wird das Ausführen eines Skripts beschrieben.

**So führen Sie ein Skript aus**

1.  Kopieren Sie den Code, und speichern Sie ihn in einer Datei mit der Erweiterung .vbs, z. *B.filename.vbs*. Stellen Sie sicher, dass Ihr Text-Editor der .txt datei keine Erweiterung hinzufüge.
2.  Öffnen Sie ein Eingabeaufforderungsfenster, und navigieren Sie zu dem Verzeichnis, in dem Sie die Datei gespeichert haben.
3.  Geben **Sie cscript filename.vbs** eingabeaufforderung ein.
4.  Wenn Sie nicht auf ein Ereignisprotokoll zugreifen können, überprüfen Sie, ob Sie über eine Eingabeaufforderung mit erhöhten Rechten ausführen. Einige Ereignisprotokollen, z. B. das Sicherheitsereignisprotokoll, können durch Benutzerzugriffssteuerungen (User Access Controls, UAC) geschützt werden.

> [!Note]  
> Standardmäßig zeigt cscript die Ausgabe eines Skripts im Eingabeaufforderungsfenster an. Da WMI-Skripts große Mengen an Ausgabe erzeugen können, sollten Sie die Ausgabe an eine Datei umleiten. Geben **Sie cscript filename.vbs > outfile.txt** eingabeaufforderung ein,  um die Ausgabe des skriptsfilename.vbsan *outfile.txt.*

 

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
<td>... Stellen Sie mit WMI eine Verbindung mit einem Remotecomputer her?</td>
<td>Geben Sie eine der folgenden Angaben als Teil der <a href="constructing-a-moniker-string.md">Moniker-Verbindungszeichenfolge</a> an:<br/>
<ul>
<li>Ein NetBIOS-Computername, z. B. &quot; atl-dc-01&quot;</li>
<li>Ein vollqualifizierter Domänenname, z. &quot; B. atl-dc-01.fabrikam.com&quot;</li>
<li>Eine IPv4-Adresse, z. &quot; B. 192.168.1.1&quot;</li>
<li>Ab Windows Vista können Sie eine IPv6-Adresse angeben, wenn der Zielcomputer und der Computer, von dem aus Sie die Verbindung herstellen, IPv6 ausführen.<br/></li>
</ul>
Weitere Informationen finden Sie unter Herstellen einer Verbindung mit <a href="connecting-to-wmi-on-a-remote-computer.md">WMI auf</a> einem Remotecomputer und <a href="ipv6-and-ipv4-support-in-wmi.md">IPv6- und IPv4-Unterstützung in WMI.</a><br/> <span data-codelanguage="VisualBasic"></span>
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
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... Ein WMI-Skript unter alternativen Anmeldeinformationen ausführen?</td>
<td><p>Verwenden Sie <a href="swbemlocator-connectserver.md"><strong>die SWbemLocator.ConnectServer-Methode</strong></a> oder <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator::ConnectServer</strong></a> in C++, und fügen Sie den entsprechenden Benutzernamen und das Kennwort ein. Sie können die Anmeldeinformationen nicht ändern, wenn Sie eine Verbindung mit dem lokalen Computer herstellen. Weitere Informationen finden Sie unter <a href="creating-a-wmi-script.md">Erstellen eines WMI-Skripts und</a> Herstellen einer Verbindung mit <a href="connecting-to-wmi-on-a-remote-computer.md">WMI auf einem Remotecomputer.</a></p>
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
<col  />
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

[WMI-Aufgaben für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Beispiele für WMI-C++-Anwendungen](wmi-c---application-examples.md)
</dt> <dt>

[TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
