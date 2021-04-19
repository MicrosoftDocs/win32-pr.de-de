---
description: Wilogutl.exe unterstützt die Analyse von Protokolldateien von einer Windows Installer-Installation und zeigt vorgeschlagene Lösungen für Fehler an, die in einer Protokolldatei gefunden werden.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81c3c82299a08fd947fbbecc7afd8a373252b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357128"
---
# <a name="wilogutlexe"></a>Wilogutl.exe

Wilogutl.exe unterstützt die Analyse von Protokolldateien von einer Windows Installer-Installation und zeigt vorgeschlagene Lösungen für Fehler an, die in einer Protokolldatei gefunden werden.

Nicht kritische Fehler werden nicht angezeigt. Wilogutl.exe können im stillen Modus oder mit einer Benutzeroberfläche (UI) ausgeführt werden. Das Tool generiert Berichte als Textdateien sowohl in der Benutzeroberfläche als auch in den stillen Modi. Dies funktioniert am besten mit ausführlichen Windows Installer Protokolldateien, funktioniert aber auch mit nicht ausführlichen Protokollen. Weitere Informationen finden Sie unter [Protokollierung](logging.md).

Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

## <a name="syntax"></a>Syntax

**wilogutl.exe***\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*

Sie können die folgenden Befehlszeilen verwenden, um im stillen Modus auszuführen.

**Wilogutl/q/l** *c: \\ mymsilog. log* **/o** *c \\ OutputDir \\*

**Wilogutl/q/l** *c: \\ mymsilog. log*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Wilogutl.exe verwendet die folgenden Befehlszeilenoptionen ohne Beachtung der Groß-/Kleinschreibung. Ein Bindestrich-Trennzeichen kann anstelle eines Schrägstrichs verwendet werden.



| Option | BESCHREIBUNG                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| none   | Wird im Benutzeroberflächen Modus ausgeführt – ohne Befehlszeilenoptionen.                                                                                                                                                   |
| /q     | Gibt den stillen Modus an. Wilogutl.exe generiert Berichtsdateien und zeigt keine Benutzeroberfläche an.                                                                                            |
| /l     | Gibt den Namen der Protokolldatei an, die analysiert werden soll. Diese Option ist erforderlich, wenn Sie den stillen Modus verwenden.                                                                                           |
| /o     | Gibt das Ausgabeverzeichnis für Berichtsdateien an. Dieser Ausgabepfad wird nur verwendet, wenn er im stillen Modus ausgeführt wird. Wenn die Option nicht vorhanden ist, werden die Berichte in das Verzeichnis "C: \\ wilogresults" eingefügt. |



 

Wenn Sie den Benutzeroberflächen Modus ausführen, werden in Wilogutl.exe die folgenden Dialogfelder angezeigt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Installer Verbose Log Analyzer</td>
<td>Im Dialogfeld Windows Installer Verbose Log Analyzer können Benutzer eine Protokolldatei für die Analyse auswählen:
<ul>
<li>Die Schaltfläche <strong>Öffnen</strong> öffnet die Datei im Editor. Der Vorschaubereich kann verwendet werden, um zu überprüfen, ob die richtige Protokolldatei ausgewählt wurde.</li>
<li>Mit der Schaltfläche <strong>analysieren</strong> wird die Protokolldatei Analyse gestartet, und das Dialogfeld ausführliche Protokolldatei Ansicht wird angezeigt.</li>
</ul></td>
</tr>
<tr class="even">
<td>Ausführliche Protokolldatei Ansicht</td>
<td>Im Dialogfeld ausführliche Protokolldatei Ansicht werden protokollierte Fehlerinformationen angezeigt. Verwenden Sie die Schaltflächen <strong>zurück</strong> und <strong>weiter</strong> , um durch mehrere Fehler zu navigieren. Aktivieren Sie das Kontrollkästchen <strong>ignorierte Debugfehler anzeigen</strong> , um nicht kritische Fehler anzuzeigen. Die Installer-Version auf dem Computer, der zum Ausführen der protokollierten Installation verwendet wird, wird angezeigt. Wenn die protokollierte Installation mit erweiterten Berechtigungen ausgeführt wurde, ist das Kontrollkästchen <strong>Installation mit erhöhten</strong> rechten aktiviert, und Informationen finden Sie in den Textfeldern Details zu den <strong>Client seitigen</strong> Berechtigungen und <strong>Details zur Server seitigen Berechtigung</strong> . Das Dialogfeld ausführliche Protokolldatei Ansicht enthält die folgenden Schaltflächen:<br/>
<ul>
<li><strong>Zustände</strong> - Zeigt das Dialogfeld Funktions-und Komponenten Zustände an.</li>
<li><strong>Eigenschaften</strong> - Zeigen Sie das Dialogfeld Eigenschaften an.</li>
<li><strong>Richtlinien</strong> - Zeigen Sie das Dialogfeld Richtlinien an.</li>
<li><strong>HTML-Protokoll</strong> - mit Anmerkungen Protokoll als mit Anmerkungen versehene HTML-Datei anzeigen.</li>
<li><strong>Ergebnisse speichern</strong> - Speichert Berichtsdateien im angegebenen Verzeichnis.</li>
<li><strong>Hilfe zu</strong> - Fehlermeldungen Hilfe zur Installationsprogramm Fehlermeldung anzeigen.</li>
<li><strong>Hilfe</strong> - Anzeigen der Hilfe für Windows Installer Setup Log Analyzer.</li>
<li>Vorgehens <strong>Weise beim Lesen einer Protokolldatei</strong> - Zeigen Sie das Hilfedokument für die Protokolldatei an.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Funktions-und Komponenten Zustände</td>
<td>Im Dialogfeld <strong>Funktions-und Komponenten Zustände</strong> werden die Status der Features und Komponenten angezeigt:
<ul>
<li>In der Spalte <strong>Feature</strong> wird der Name der Funktion im Installationspaket angezeigt.</li>
<li>In der Spalte <strong>Komponente</strong> wird der Name der Komponente im Installationspaket angezeigt.</li>
<li>In der Spalte <strong>installiert</strong> wird der Zustand oder der Zustand der Komponente am Ende der Installation angezeigt.</li>
<li>In der Spalte <strong>Anforderung</strong> wird die Auswahl des Benutzers während der Installation für den Funktions-oder Komponenten Zustand angezeigt.</li>
<li>In der Spalte <strong>Aktion</strong> wird die Aktion angezeigt, die vom Installationsprogramm für das Feature oder die Komponente ausgeführt wird.</li>
</ul>
Weitere Informationen finden Sie unter <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> und <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.<br/></td>
</tr>
<tr class="even">
<td>Eigenschaften</td>
<td>Im Dialogfeld Eigenschaften werden Windows Installer <a href="properties.md">Eigenschaften</a> und deren Werte am Ende der Installation angezeigt. Sie können die Eigenschaften nach Name oder Wert sortieren:
<ul>
<li>Auf der Registerkarte <strong>Client</strong> werden Eigenschaften und Werte während des Client seitigen Teils der Installation angezeigt.</li>
<li>Die Registerkarte <strong>Server</strong> zeigt Eigenschaften und Werte während des Server Teils der Installation an.</li>
<li>Die <strong>Registerkarte</strong> "neu" zeigt die Eigenschaften und Werte aller <a href="concurrent-installations.md">gleichzeitigen Installationen</a>an.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Richtlinien</td>
<td>Im Dialogfeld Richtlinien wird die <a href="system-policy.md">System Richtlinie</a> angezeigt, die nach der Installation festgelegt wurde:
<ul>
<li>Der für die Richtlinie festgelegte Wert 0 (null) bedeutet, dass die Richtlinie nicht aktiviert ist.</li>
<li>Der Wert 1 (eins) bedeutet, dass die Richtlinie aktiviert ist.</li>
<li>Der Wert? (Fragezeichen) bedeutet, dass der Richtlinien Wert nicht im Protokoll aufgezeichnet wird.</li>
</ul>
Wenn Sie einen Richtlinien Wert benötigen, der nicht im Protokoll angezeigt wird, verwenden Sie Regedit.exe, um die Registrierungsschlüssel auf dem Computer zu überprüfen, der die Installation nicht bestanden hat.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="report-files"></a>Berichtsdateien

Wenn Sie im Dialog **Feld ausführliche Protokolldatei Ansicht** eine Analyse im stillen Modus durchführen oder auf die Schaltfläche **Ergebnisse speichern** klicken, generiert das Windows Installer Setup Analyzer-Tool drei Textdateien und eine mit Anmerkungen versehene Protokolldatei.

In der folgenden Tabelle sind die Namen und Inhalte der Berichtsdateien aufgeführt.



| Name                      | BESCHREIBUNG                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Protokoll Dateiname- \_summary.txt  | Fasst die Protokolldatei zusammen. Listet die Informationen auf, die im Dialogfeld ausführliche Protokolldatei Ansicht und der erste Fehler angezeigt werden.         |
| Protokoll Dateiname- \_errors.txt   | Gibt die Anzahl von Fehlern, die Fehler und die empfohlenen Lösungen an. In dieser Datei werden sowohl kritische als auch nicht kritische Fehler aufgeführt. |
| Protokoll Dateiname- \_policies.txt | Identifiziert die Richtlinien Namen und Werte, die am Ende der Installation wie im Dialogfeld Richtlinien festgelegt werden.                       |
| Details \_logfilename.htm  | Ein HTML-Protokoll mit Anmerkungen und einer Legende für die Farbcodierung.                                                                      |



 

## <a name="return-values"></a>Rückgabewerte

Wenn für Vorgänge im stillen Modus ungültige Befehlszeilenargumente weitergegeben werden, führt Wilogutl.exe keine Aktion aus, und der Prozess gibt einen der Werte in der folgenden Tabelle zurück.



| Wert | Bedeutung                                                                 |
|-------|-------------------------------------------------------------------------|
| 1     | Es wurde ein ungültiges Ausgabeverzeichnis angegeben.                                      |
| 2     | Es wurde ein ungültiger Protokoll Dateiname angegeben.                                         |
| 3     | Der/q wurde erfolgreich, jedoch fehlt der erforderliche Switch/l für den Namen der Protokolldatei. |
| 4     | Der/l wurde erfolgreich ausgeführt, jedoch fehlt der erforderliche Switch/q für den stillen Modus.        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
</dt> </dl>

 

 




