---
title: Sammeln von User-Mode Dumps
description: Ab Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) können Windows-Fehlerberichterstattung (wer) so konfiguriert werden, dass vollständige benutzermodusdumps gesammelt und lokal gespeichert werden, nachdem eine Anwendung im Benutzermodus abstürzt.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7b1e7850e84d9fa6c8d10953d23640b41b1bc6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858163"
---
# <a name="collecting-user-mode-dumps"></a>Sammeln von User-Mode Dumps

Ab Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) können Windows-Fehlerberichterstattung (wer) so konfiguriert werden, dass vollständige benutzermodusdumps gesammelt und lokal gespeichert werden, nachdem eine Anwendung im Benutzermodus abstürzt. Anwendungen, die eigene benutzerdefinierte Absturzberichte ausführen, einschließlich .NET-Anwendungen, werden von dieser Funktion nicht unterstützt.

Diese Funktion ist standardmäßig nicht aktiviert. Zum Aktivieren des Features sind Administratorrechte erforderlich. Um die Funktion zu aktivieren und zu konfigurieren, verwenden Sie die folgenden Registrierungs Werte unter dem Schlüssel **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ Windows-Fehlerberichterstattung \\ localdumps** Key.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>BESCHREIBUNG</th>
<th>type</th>
<th>Standardwert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Dumpfolder</strong></td>
<td>Der Pfad, in dem die Dumpdateien gespeichert werden sollen. Wenn Sie nicht den Standardpfad verwenden, stellen Sie sicher, dass der Ordner ACLs enthält, die es dem Absturz Prozess ermöglichen, Daten in den Ordner zu schreiben. Für Dienst Abstürze wird das Dump abhängig vom verwendeten Dienst Konto in Dienst spezifische Profilordner geschrieben. Beispielsweise lautet der Profilordner für System Dienste%windir%\system32\config\systemprofile. Für Netzwerkdienste und lokale Dienste lautet der Ordner%windir%\serviceprofiles.<br/></td>
<td>REG_EXPAND_SZ</td>
<td>%LocalAppData%\crashdumps</td>
</tr>
<tr class="even">
<td><strong>Dumpcount</strong></td>
<td>Die maximale Anzahl von Dumpdateien im Ordner. Wenn der Höchstwert überschritten wird, wird die älteste Dumpdatei im Ordner durch die neue Dumpdatei ersetzt.</td>
<td>REG_DWORD</td>
<td>10</td>
</tr>
<tr class="odd">
<td><strong>Dumptype</strong></td>
<td>Geben Sie einen der folgenden dumptypen an:
<ul>
<li>0: benutzerdefiniertes Dump</li>
<li>1: Mini Abbild</li>
<li>2: vollständiges Dump</li>
</ul></td>
<td>REG_DWORD</td>
<td>1</td>
</tr>
<tr class="even">
<td><strong>Customdumpflags</strong></td>
<td>Die benutzerdefinierten dumpoptionen, die verwendet werden sollen. Dieser Wert wird nur verwendet, wenn <strong>dumptype</strong> auf 0 festgelegt ist.<br/> Bei den Optionen handelt es sich um eine bitweise Kombination der <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> Enumerationswerte.<br/></td>
<td>REG_DWORD</td>
<td><code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData.</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> Beim Festlegen [des automatischen Debuggens für **Anwendungs** Abstürze](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes)wird kein Absturz Abbild erfasst. 

Diese Registrierungs Werte stellen die globalen Einstellungen dar. Sie können auch anwendungsspezifische Einstellungen angeben, die die globalen Einstellungen außer Kraft setzen. Erstellen Sie einen neuen Schlüssel für Ihre Anwendung unter **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ Windows-Fehlerberichterstattung \\ localdumps** (z. b. **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ Windows-Fehlerberichterstattung \\ localdumps \\MyApplication.exe**), um eine Einstellung pro Anwendung zu erstellen. Fügen Sie die dumpeinstellungen unter dem **MyApplication.exe** -Schlüssel hinzu. Wenn die Anwendung abstürzt, liest wer zuerst die globalen Einstellungen und setzt dann alle Einstellungen mit den anwendungsspezifischen Einstellungen außer Kraft.

Nachdem eine Anwendung abstürzt und vor deren Beendigung, überprüft das System die Registrierungs Einstellungen, um zu bestimmen, ob ein lokales Dump gesammelt werden soll. Nachdem die dumpsammlung abgeschlossen wurde, kann die Anwendung normal beendet werden. Wenn die Anwendung die Wiederherstellung unterstützt, wird das lokale Dump vor dem Aufrufen des Wiederherstellungs Rückrufs gesammelt.

Diese Abbilder werden unabhängig vom Rest der Wer-Infrastruktur konfiguriert und gesteuert. Sie können die lokale dumpsammlung auch dann verwenden, wenn wer deaktiviert ist oder der Benutzer die wer-Berichterstattung abbricht. Das lokale Abbild kann sich von dem an Microsoft gesendeten Dump unterscheiden.

 

