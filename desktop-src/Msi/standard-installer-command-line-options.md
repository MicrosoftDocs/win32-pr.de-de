---
description: Das ausführbare Programm, das Pakete interpretiert und Produkte installiert, ist Msiexec.exe. Beachten Sie, dass Msiexec bei der Rückgabe auch eine Fehlerebene festlegt, die Systemfehlercodes entspricht. In der folgenden Tabelle sind die Standardbefehlszeilenoptionen für dieses Programm aufgeführt. Bei Befehlszeilenoptionen wird die Groß-/Kleinschreibung nicht beachtet. Windows Installer 2.0: Die in diesem Thema identifizierten Befehlszeilenoptionen sind ab Windows Installer 3.0 verfügbar. Die Windows Installer Command-Line Optionen sind mit Windows Installer&\# 160;3.0 und früheren Versionen verfügbar.
ms.assetid: b1707c88-1cca-45ab-bb23-6002bfd5204e title: Standard Installer Command-Line Options ms.topic: article ms.date: 05/31/2018
---

# <a name="standard-installer-command-line-options"></a>Standardinstallationsprogramm Command-Line Optionen

Das ausführbare Programm, das Pakete interpretiert und Produkte installiert, ist Msiexec.exe.

> [!Note]  
> Msiexec legt bei der Rückgabe auch eine Fehlerebene fest, die [systemfehlercodes](../debug/system-error-codes.md)entspricht.

 

In der folgenden Tabelle sind die Standardbefehlszeilenoptionen für dieses Programm aufgeführt. Bei Befehlszeilenoptionen wird die Groß-/Kleinschreibung nicht beachtet.

**Windows Installer 2.0:** Die in diesem Thema identifizierten Befehlszeilenoptionen sind ab Windows Installer 3.0 verfügbar. Die [Befehlszeilenoptionen](command-line-options.md) für Windows Installer sind mit Windows Installer 3.0 und früheren Versionen verfügbar.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>Hilfe- und Kurzübersichtsoption. Zeigt die richtige Verwendung des Setupbefehls an, einschließlich einer Liste aller Switches und des Verhaltens. Die Beschreibung der Nutzung kann auf der Benutzeroberfläche angezeigt werden. Diese Hilfeoption wird durch eine falsche Verwendung einer Option aufgerufen.<br/> Beispiel: <strong>msiexec /help</strong><br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows <a href="command-line-options.md">Installer-Befehlszeilenoption</a> ist <strong>/?</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/quiet</strong></td>
<td> </td>
<td>Stille Anzeigeoption. Das Installationsprogramm führt eine Installation aus, ohne eine Benutzeroberfläche anzuzeigen. Dem Benutzer werden keine Eingabeaufforderungen, Meldungen oder Dialogfelder angezeigt. Der Benutzer kann die Installation nicht abbrechen. Verwenden Sie die Standardbefehlszeilenoptionen <strong>/norestart</strong> oder <strong>/forcerestart,</strong> um Neustarts zu steuern. Wenn keine Neustartoptionen angegeben sind, startet das Installationsprogramm den Computer bei Bedarf neu, ohne dem Benutzer eine Eingabeaufforderung oder Warnung anzuzeigen.<br/> Beispiele: <br/> <strong>msiexec /package Application.msi /quiet</strong><br/> <strong>Msiexec /uninstall Application.msi /quiet</strong><br/> <strong>Msiexec /update msipatch.msp /quiet</strong><br/> <strong>Msiexec /uninstall msipatch.msp /package Application.msi/quiet</strong><br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows <a href="command-line-options.md">Installer-Befehlszeilenoption</a> ist <strong>/qn.</strong>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/passive</strong></td>
<td> </td>
<td>Passive Anzeigeoption. Das Installationsprogramm zeigt dem Benutzer eine Statusanzeige an, die angibt, dass eine Installation ausgeführt wird, aber dem Benutzer keine Eingabeaufforderungen oder Fehlermeldungen angezeigt werden. Der Benutzer kann die Installation nicht abbrechen. Verwenden Sie die Standardbefehlszeilenoptionen <strong>/norestart</strong> oder <strong>/forcerestart,</strong> um Neustarts zu steuern. Wenn keine Neustartoption angegeben ist, startet das Installationsprogramm den Computer bei Bedarf neu, ohne dem Benutzer eine Eingabeaufforderung oder Warnung anzuzeigen. <br/> Beispiel: <strong>msiexec /package Application.msi /passive</strong> <br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows <a href="command-line-options.md">Installer-Befehlszeilenoption</a> ist <strong>/qb!-,</strong> wobei <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>=S in der Befehlszeile festgelegt ist.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/norestart</strong></td>
<td> </td>
<td>Option "Nie neu starten". Das Installationsprogramm startet den Computer nach der Installation nie neu.<br/> Beispiel: msiexec /package Application.msi <strong>/norestart</strong><br/>
<blockquote>
[!Note]<br />
Für die entsprechende Windows Installer-Befehlszeile ist <a href="reboot.md"><strong>REBOOT</strong></a>=ReallySuppress in der Befehlszeile festgelegt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/forcerestart</strong></td>
<td> </td>
<td>Option "Immer neu starten". Das Installationsprogramm startet den Computer nach jeder Installation immer neu.<br/> Beispiel: msiexec /package Application.msi <strong>/forcerestart</strong><br/>
<blockquote>
[!Note]<br />
Für die entsprechende Windows Installer-Befehlszeile ist <a href="reboot.md"><strong>REBOOT</strong></a>=Force in der Befehlszeile festgelegt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/promptrestart</strong></td>
<td> </td>
<td>Eingabeaufforderung vor Neustartoption. Zeigt eine Meldung an, dass ein Neustart erforderlich ist, um die Installation abzuschließen, und fragt den Benutzer, ob das System jetzt neu gestartet werden soll. Diese Option kann nicht zusammen mit der Option <strong>/quiet</strong> verwendet werden.<br/>
<blockquote>
[!Note]<br />
Für die entsprechende Windows Installer-Befehlszeile ist <a href="rebootprompt.md"><strong>REBOOTPROMPT</strong></a>  =  &quot; &quot; in der Befehlszeile festgelegt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/uninstall</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Option "Produkt deinstallieren". Deinstalliert ein Produkt.<br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows <a href="command-line-options.md">Installer-Befehlszeilenoption</a> ist <strong>/x.</strong>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/uninstall</strong></td>
<td><em>/package <Package.msi | ProductCode> /uninstall <Update1.msp | PatchGUID1> [; Update2.msp-| PatchGUID2]</em></td>
<td>Option "Update deinstallieren". Deinstalliert einen Updatepatch.<br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows <a href="command-line-options.md">Installer-Befehlszeilenoption</a> ist <strong>/I</strong> mit <a href="msipatchremove.md"><strong>MSIPATCHREMOVE</strong></a>=Update1.msp | PatchGUID1[; Update2.msp-| PatchGUID2] in der Befehlszeile festgelegt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/log</strong></td>
<td><em><logfile></em></td>
<td>Protokolloption. Schreibt Protokollierungsinformationen unter dem angegebenen vorhandenen Pfad in eine Protokolldatei. Der Pfad zum Speicherort der Protokolldatei muss bereits vorhanden sein. Das Installationsprogramm erstellt nicht die Verzeichnisstruktur für die Protokolldatei.<br/> Die folgenden Informationen werden in das Protokoll eingegeben:<br/>
<ul>
<li>Statusmeldungen</li>
<li>Nichttale Warnungen</li>
<li>Alle Fehlermeldungen</li>
<li>Starten von Aktionen</li>
<li>Aktionsspezifische Datensätze</li>
<li>Benutzeranforderungen</li>
<li>Parameter der ersten Benutzeroberfläche</li>
<li>Informationen zu nicht genügend Arbeitsspeicher oder schwerwiegenden Beendigungsinformationen</li>
<li>Nachrichten mit nicht genügend Speicherplatz</li>
<li>Terminaleigenschaften</li>
</ul>
<blockquote>
[!Note]<br />
Die entsprechende Windows <a href="command-line-options.md">Installer-Befehlszeilenoption</a> ist <strong>/L*.</strong>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Weitere Informationen zu allen Methoden, die zum Festlegen des Protokollierungsmodus verfügbar sind, finden Sie im Abschnitt Protokollierung des <a href="windows-installer-logging.md">Windows Installers</a> unter Normale <a href="normal-logging.md">Protokollierung.</a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>/package</strong></td>
<td><em><Package.msi|ProductCode></em></td>
<td>Option "Produkt installieren". Installiert oder konfiguriert ein Produkt.<br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows <a href="command-line-options.md">Installer-Befehlszeilenoption</a> ist <strong>/I.</strong>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/update</strong></td>
<td><em><Update1.msp>[; Update2.msp]</em></td>
<td>Option "Patches installieren". Installiert ein oder mehrere Patches. <br/>
<blockquote>
[!Note]<br />
Die entsprechende Windows Installer-Befehlszeile weist <a href="patch.md"><strong>PATCH</strong></a> = [msipatch.msp]<; PatchGuid2> in der Befehlszeile festgelegt.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
