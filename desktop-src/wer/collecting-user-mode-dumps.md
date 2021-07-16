---
title: Sammeln von User-Mode Dumps
description: Ab Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) können Windows-Fehlerberichterstattung (WER) so konfiguriert werden, dass vollständige Speicherabbilder im Benutzermodus erfasst und lokal gespeichert werden, nachdem eine Anwendung im Benutzermodus abstürzt.
ms.assetid: 8dad892b-04df-4aeb-b6c4-82f7676d382a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6291d3ad8dfeb641582a93f6789ca7844594ad
ms.sourcegitcommit: 892997f4126d44df413286074e08a9c6065313ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2021
ms.locfileid: "114300185"
---
# <a name="collecting-user-mode-dumps"></a>Sammeln von User-Mode Dumps

Ab Windows Server 2008 und Windows Vista mit Service Pack 1 (SP1) können Windows-Fehlerberichterstattung (WER) so konfiguriert werden, dass vollständige Speicherabbilder im Benutzermodus erfasst und lokal gespeichert werden, nachdem eine Anwendung im Benutzermodus abstürzt. Anwendungen, die ihre eigene benutzerdefinierte Absturzberichterstellung durchführen, einschließlich .NET-Anwendungen, werden von diesem Feature nicht unterstützt.

Diese Funktion ist standardmäßig nicht aktiviert. Zum Aktivieren des Features sind Administratorrechte erforderlich. Verwenden Sie zum Aktivieren und Konfigurieren des Features die folgenden Registrierungswerte unter **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows Windows-Fehlerberichterstattung \_ \\ \\ \\ \\ \\ LocalDumps-Schlüssel.**

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
<th>Typ</th>
<th>Standardwert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>DumpFolder</strong></td>
<td>Der Pfad, in dem die Dumpdateien gespeichert werden sollen. Wenn Sie den Standardpfad nicht verwenden, stellen Sie sicher, dass der Ordner ACLs enthält, die es dem abstürzenden Prozess ermöglichen, Daten in den Ordner zu schreiben. Bei Dienstabstürzen wird das Speicherabbild abhängig vom verwendeten Dienstkonto in dienstspezifische Profilordner geschrieben. Der Profilordner für Systemdienste lautet beispielsweise %WINDIR%\System32\Config\SystemProfile. Für Netzwerk- und lokale Dienste lautet der Ordner %WINDIR%\ServiceProfiles.<br/></td>
<td>Reg_expand_sz</td>
<td>%LOCALAPPDATA%\CrashDumps</td>
</tr>
<tr class="even">
<td><strong>DumpCount</strong></td>
<td>Die maximale Anzahl von Sicherungsdateien im Ordner. Wenn der maximale Wert überschritten wird, wird die älteste Speicherabbilddatei im Ordner durch die neue Dumpdatei ersetzt.</td>
<td>REG_DWORD</td>
<td>10</td>
</tr>
<tr class="odd">
<td><strong>DumpType</strong></td>
<td>Geben Sie einen der folgenden Speicherabbildtypen an:
<ul>
<li>0: Benutzerdefiniertes Speicherabbild</li>
<li>1: Miniabbild</li>
<li>2: Vollständiges Speicherabbild</li>
</ul></td>
<td>REG_DWORD</td>
<td>1</td>
</tr>
<tr class="even">
<td><strong>CustomDumpFlags</strong></td>
<td>Die zu verwendenden benutzerdefinierten Speicherabbildoptionen. Dieser Wert wird nur verwendet, wenn <strong>DumpType</strong> auf 0 festgelegt ist.<br/> Die Optionen sind eine bitweise Kombination der <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type"><strong>MINIDUMP_TYPE</strong></a> Enumerationswerte.<br/></td>
<td>REG_DWORD</td>
 <td><code>0x00000121</code> (<code>MiniDumpWithDataSegs | MiniDumpWithUnloadedModules | MiniDumpWithProcessThreadData == 0x00000001 | 0x00000020 | 0x00000100)</code></td>
</tr>
</tbody>
</table>

>[!NOTE]
> Ein Absturzabbild wird nicht erfasst, wenn Sie [das automatische Debuggen für **Anwendungsabstürze**](../debug/configuring-automatic-debugging.md#configuring-automatic-debugging-for-application-crashes)festlegen. 

Diese Registrierungswerte stellen die globalen Einstellungen dar. Sie können auch Anwendungsspezifische Einstellungen angeben, die die globalen Einstellungen außer Kraft setzen. Um eine Anwendungseinstellung zu erstellen, erstellen Sie einen neuen Schlüssel für Ihre Anwendung unter **HKEY \_ LOCAL MACHINE Software Microsoft Windows Windows-Fehlerberichterstattung \_ \\ \\ \\ \\ \\ LocalDumps** (z.B. **HKEY LOCAL MACHINE Software \_ Microsoft Windows Windows-Fehlerberichterstattung \_ \\ \\ \\ \\ \\ LocalDumps \\MyApplication.exe**). Fügen Sie Ihre Speicherabbildeinstellungen unter dem **MyApplication.exe** Schlüssel hinzu. Wenn Ihre Anwendung abstürzt, liest WER zuerst die globalen Einstellungen und überschreibt dann alle Einstellungen mit Ihren anwendungsspezifischen Einstellungen.

Nach dem Absturz einer Anwendung und vor dem Beenden überprüft das System die Registrierungseinstellungen, um zu ermitteln, ob ein lokales Speicherabbild erfasst werden soll. Nach Abschluss der Speicherabbildsammlung kann die Anwendung normal beendet werden. Wenn die Anwendung die Wiederherstellung unterstützt, wird das lokale Speicherabbild erfasst, bevor der Wiederherstellungsrückruf aufgerufen wird.

Diese Dumps werden unabhängig von der restlichen WER-Infrastruktur konfiguriert und gesteuert. Sie können die lokale Speicherabbildsammlung auch dann verwenden, wenn WER deaktiviert ist oder der Benutzer die WER-Berichterstellung abbricht. Das lokale Speicherabbild kann sich von dem an Microsoft gesendeten Dump unterscheiden.

 

