---
Beschreibung: das ausführbare Programm zum Interpretieren von Paketen und zum Installieren von Produkten ist Msiexec.exe. Beachten Sie, dass msiexec bei der Rückgabe auch eine Fehlerstufe festlegt, die System Fehler Codes entspricht. In der folgenden Tabelle sind die standardmäßigen Befehlszeilenoptionen für dieses Programm aufgeführt. Befehlszeilenoptionen Unterscheidung nach Groß-/Kleinschreibung. Windows Installer 2,0: die in diesem Thema identifizierten Befehlszeilenoptionen sind ab Windows Installer 3,0 verfügbar. Die Windows Installer Command-Line Optionen sind in Windows Installer&\# 160; 3.0 und früheren Versionen verfügbar.
ms. assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e Title: Standard-Installer Command-Line Optionen ms. Topic: article ms. Date: 05/31/2018
---

# <a name="standard-installer-command-line-options"></a>Standard Installations Command-Line Optionen

Das ausführbare Programm, das Pakete interpretiert und Produkte installiert, ist Msiexec.exe.

> [!Note]  
> Msiexec legt außerdem eine Fehlerstufe für die Rückgabe fest, die [System Fehler Codes](../debug/system-error-codes.md)entspricht.

 

In der folgenden Tabelle sind die standardmäßigen Befehlszeilenoptionen für dieses Programm aufgeführt. Befehlszeilenoptionen Unterscheidung nach Groß-/Kleinschreibung.

**Windows Installer 2,0:** Die Befehlszeilenoptionen, die in diesem Thema identifiziert werden, sind ab Windows Installer 3,0 verfügbar. Die Windows Installer [Befehlszeilenoptionen](command-line-options.md) sind in Windows Installer 3,0 und früheren Versionen verfügbar.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Parameter</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/help</strong></td>
<td> </td>
<td>Hilfe und Quick Reference-Option. Zeigt die korrekte Verwendung des Setup-Befehls einschließlich einer Liste aller Switches und des Verhaltens an. Die Beschreibung der Verwendung kann in der Benutzeroberfläche angezeigt werden. Die falsche Verwendung einer beliebigen Option ruft diese Hilfe Option auf.<br/> Beispiel: <strong>msiexec/Help</strong><br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/?</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/quiet</strong></td>
<td> </td>
<td>Option zur stillen Anzeige. Das Installationsprogramm führt eine Installation aus, ohne eine Benutzeroberfläche anzuzeigen. Dem Benutzer werden keine Eingabe Aufforderungen, Meldungen oder Dialogfelder angezeigt. Der Benutzer kann die Installation nicht abbrechen. Verwenden Sie die <strong>/norestart</strong> -oder <strong>/forcerestart</strong> -Standard Befehlszeilenoptionen, um Neustarts zu steuern. Wenn keine Neustart Optionen angegeben werden, wird der Computer vom Installer bei Bedarf neu gestartet, ohne dass dem Benutzer eine Eingabeaufforderung oder eine Warnung angezeigt wird.<br/> Beispiele: <br/> <strong>msiexec/Package Application.msi/quiet</strong><br/> <strong>Msiexec/Uninstall Application.msi/quiet</strong><br/> <strong>Msiexec/Update msipatch. msp/quiet</strong><br/> <strong>Msiexec/Uninstall msipatch. msp/Package Application.msi/quiet</strong><br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/QN</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/passive</strong></td>
<td> </td>
<td>Passive Anzeigeoption. Das Installationsprogramm zeigt dem Benutzer eine Statusanzeige an, die anzeigt, dass eine Installation ausgeführt wird, dem Benutzer jedoch keine Eingabe Aufforderungen oder Fehlermeldungen angezeigt werden. Der Benutzer kann die Installation nicht abbrechen. Verwenden Sie die <strong>/norestart</strong> -oder <strong>/forcerestart</strong> -Standard Befehlszeilenoptionen, um Neustarts zu steuern. Wenn keine Neustart Option angegeben ist, wird der Computer vom Installer bei Bedarf neu gestartet, ohne dass dem Benutzer eine Eingabeaufforderung oder eine Warnung angezeigt wird. <br/> Beispiel: <strong>msiexec/Package Application.msi/passive</strong> <br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/qb!-</strong> with <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>= S wird in der Befehlszeile festgelegt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/norestart</strong></td>
<td> </td>
<td>Option nie neu starten. Das Installationsprogramm startet den Computer nach der Installation nie neu.<br/> Beispiel: msiexec/Package Application.msi <strong>/norestart</strong><br/>
<blockquote>
[!Note]<br />
In der entsprechenden Windows Installer Befehlszeile ist <a href="reboot.md"><strong>Reboot</strong></a>= reallyunterdrückung in der Befehlszeile festgelegt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/forcerestart</strong></td>
<td> </td>
<td>Option "immer neu starten". Das Installationsprogramm startet den Computer nach jeder Installation immer neu.<br/> Beispiel: msiexec/Package Application.msi <strong>/forcerestart</strong><br/>
<blockquote>
[!Note]<br />
In der entsprechenden Windows Installer Befehlszeile ist <a href="reboot.md"><strong>Reboot</strong></a>= Force in der Befehlszeile festgelegt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/promptrestart</strong></td>
<td> </td>
<td>Eingabeaufforderung vor Neustarts. Zeigt eine Meldung an, dass ein Neustart erforderlich ist, um die Installation abzuschließen, und fragt den Benutzer, ob das System jetzt neu gestartet werden soll. Diese Option kann nicht in Verbindung mit der <strong>/quiet</strong> -Option verwendet werden.<br/>
<blockquote>
[!Note]<br />
In der entsprechenden Windows Installer Befehlszeile ist <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; in der Befehlszeile festgelegt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/uninstall</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Option zum Deinstallieren von Produkten. Deinstalliert ein Produkt.<br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/x</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/uninstall</strong></td>
<td><em>/Package <Package.msi | ProductCode> /Uninstall <Update1.msp | PatchGUID1> [; Update2. msp | PatchGUID2]</em></td>
<td>Option zum Deinstallieren von Updates. Deinstalliert einen Update Patch.<br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/I</strong> mit <a href="msipatchremove.md"><strong>msipatchremove</strong></a>= Update1. msp | PatchGUID1[; Update2. msp | PatchGUID2] in der Befehlszeile festgelegt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/Log</strong></td>
<td><em><logfile></em></td>
<td>Log-Option. Schreibt Protokollierungs Informationen in eine Protokolldatei unter dem angegebenen vorhandenen Pfad. Der Pfad zum Speicherort der Protokolldatei muss bereits vorhanden sein. Das Installationsprogramm erstellt nicht die Verzeichnisstruktur für die Protokolldatei.<br/> Die folgenden Informationen werden in das Protokoll eingegeben:<br/>
<ul>
<li>Statusmeldungen</li>
<li>Nicht schwerwiegende Warnungen</li>
<li>Alle Fehlermeldungen</li>
<li>Starten von Aktionen</li>
<li>Aktions spezifische Datensätze</li>
<li>Benutzer Anforderungen</li>
<li>Anfängliche Benutzeroberflächen Parameter</li>
<li>Nicht genügend Arbeitsspeicher oder schwerwiegende Beendigungs Informationen</li>
<li>Nicht genügend Speicherplatz Nachrichten</li>
<li>Terminal Eigenschaften</li>
</ul>
<blockquote>
[!Note]<br />
Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/L *</strong>.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Weitere Informationen zu allen Methoden, die zum Festlegen des Protokollierungs Modus verfügbar sind, finden Sie unter <a href="normal-logging.md">normale Protokollierung</a> im Abschnitt <a href="windows-installer-logging.md">Windows Installer Protokollierung</a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/Package</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Option zum Installieren von Produkten. Installiert oder konfiguriert ein Produkt.<br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows Installer <a href="command-line-options.md">Befehlszeilen Option</a> ist <strong>/I</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/Update</strong></td>
<td><em><Update1.msp>[; Update2. msp]</em></td>
<td>Option zum Installieren von Patches. Installiert ein oder mehrere Patches. <br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows Installer Befehlszeile enthält <a href="patch.md"><strong>Patch</strong></a> = [msipatch. msp] <; PatchGuid2> in der Befehlszeile festgelegt.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
