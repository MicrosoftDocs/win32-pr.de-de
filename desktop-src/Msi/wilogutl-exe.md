---
description: Wilogutl.exe unterstützt die Analyse von Protokolldateien aus einer installation Windows Installers und zeigt vorgeschlagene Lösungen für Fehler an, die in einer Protokolldatei gefunden werden.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6734b22afa6aa5d464f3d6b01555e54f240e006b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476026"
---
# <a name="wilogutlexe"></a>Wilogutl.exe

Wilogutl.exe unterstützt die Analyse von Protokolldateien aus einer installation Windows Installers und zeigt vorgeschlagene Lösungen für Fehler an, die in einer Protokolldatei gefunden werden.

Nicht kritische Fehler werden nicht angezeigt. Wilogutl.exe können im stillen Modus oder über eine Benutzeroberfläche (UI) ausgeführt werden. Das Tool generiert Berichte als Textdateien sowohl in der Benutzeroberfläche als auch im stillen Modus. Es funktioniert am besten mit ausführlichen Windows Installer-Protokolldateien, aber auch mit nicht ausführlichen Protokollen. Weitere Informationen finden Sie unter [Protokollierung](logging.md).

Dieses Tool ist nur in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

## <a name="syntax"></a>Syntax

**wilogutl.exe***\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*

Sie können die folgenden Befehlszeilen verwenden, um im stillen Modus auszuführen.

**willogutl /q /l** *c: \\ mymsilog.log* **/o** *c \\ outputdir \\*

**willogutl /q /l** *c: \\ mymsilog.log*

## <a name="command-line-options"></a>Befehlszeilenoptionen

Wilogutl.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird. Anstelle eines Schrägstrichs kann ein Bindestrichtrennzeichen verwendet werden.



| Option | BESCHREIBUNG                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Keine   | Wird im Benutzeroberflächenmodus ohne Befehlszeilenoptionen ausgeführt.                                                                                                                                                   |
| /q     | Gibt den stillen Modus an. Wilogutl.exe generiert Berichtsdateien und zeigt keine Benutzeroberfläche an.                                                                                            |
| /l     | Gibt den Namen der zu analysierenden Protokolldatei an. Diese Option ist bei Verwendung des stillen Modus erforderlich.                                                                                           |
| /o     | Gibt das Ausgabeverzeichnis für Berichtsdateien an. Dieser Ausgabepfad wird nur verwendet, wenn er im stillen Modus ausgeführt wird. Wenn die Option nicht vorhanden ist, werden die Berichte im Verzeichnis C: \\ WiLogResults abgelegt. |



 

Wenn sie im Benutzeroberflächenmodus ausgeführt wird, zeigt Wilogutl.exe die folgenden Dialogfelder an.




| Name | BESCHREIBUNG | 
|------|-------------|
| Windows Installer Verbose Log Analyzer | Im Dialogfeld Windows Installer Verbose Log Analyzer können Benutzer eine Protokolldatei für die Analyse auswählen:<ul><li>Die Schaltfläche <strong>Öffnen</strong> öffnet die Datei in Editor. Der Vorschaubereich kann verwendet werden, um zu überprüfen, ob die richtige Protokolldatei ausgewählt wurde.</li><li>Die Schaltfläche <strong>Analysieren</strong> beginnt mit der Protokolldateianalyse und zeigt das Dialogfeld Detaillierte Protokolldateiansicht an.</li></ul> | 
| Detaillierte Protokolldateiansicht | Im Dialogfeld Detaillierte Protokolldateiansicht werden protokollierte Fehlerinformationen angezeigt. Verwenden Sie die Schaltflächen <strong>Zurück</strong> und <strong>Weiter,</strong> um durch mehrere Fehler zu navigieren. Aktivieren Sie das Kontrollkästchen <strong>Ignorierte Debugfehler</strong> anzeigen, um nicht kritische Fehler anzuzeigen. Die Installationsprogrammversion auf dem Computer, der zum Ausführen der protokollierten Installation verwendet wird, wird angezeigt. Wenn die protokollierte Installation mit erhöhten Berechtigungen ausgeführt wurde, ist das Kontrollkästchen <strong>Erhöhte Installation</strong> aktiviert, und informationen werden in den Textfeldern <strong>Clientseitige Berechtigungsdetails</strong> und Details zu <strong>serverseitigen Berechtigungen</strong> bereitgestellt. Das Dialogfeld Detaillierte Protokolldateiansicht enthält die folgenden Schaltflächen:<br /><ul><li><strong>Status:</strong> Zeigt das Dialogfeld Funktions- und Komponentenzustände an.</li><li><strong>Eigenschaften:</strong> Zeigt das Dialogfeld Eigenschaften an.</li><li><strong>Richtlinien:</strong> Zeigt das Dialogfeld Richtlinien an.</li><li><strong>HTML-Protokoll mit Anmerkungen:</strong> Zeigt das Protokoll als HTML-Datei mit Anmerkungen an.</li><li><strong>Ergebnisse speichern:</strong> Speichern Sie Berichtsdateien im angegebenen Verzeichnis.</li><li><strong>Hilfe zu Fehlermeldungen:</strong> Zeigt die Hilfe zu Installationsfehlermeldungen an.</li><li><strong>Hilfe:</strong> Zeigt Hilfe für Windows Installer Setup Log Analyzer an.</li><li><strong>Lesen einer Protokolldatei:</strong> Zeigt das Hilfedokument zur Protokolldatei an.</li></ul> | 
| Funktions- und Komponentenzustände | Im Dialogfeld <strong>Feature- und Komponentenzustände</strong> werden die Zustände von Features und Komponenten angezeigt:<ul><li>In der Spalte <strong>Feature</strong> wird der Name des Features im Installationspaket angezeigt.</li><li>In der Spalte <strong>Komponente</strong> wird der Name der Komponente im Installationspaket angezeigt.</li><li>In der Spalte <strong>Installiert</strong> wird der Status des Features oder der Komponente am Ende der Installation angezeigt.</li><li>In der Spalte <strong>Anforderung</strong> wird die Auswahl des Benutzers während der Installation für den Zustand des Features oder der Komponente angezeigt.</li><li>In der Spalte <strong>Aktion</strong> wird die Aktion angezeigt, die vom Installationsprogramm für das Feature oder die Komponente ausgeführt wird.</li></ul>Weitere Informationen finden Sie unter <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> und <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState.</strong></a><br /> | 
| Eigenschaften | Im Dialogfeld Eigenschaften werden Windows <a href="properties.md">Installer-Eigenschaften</a> und deren Werte am Ende der Installation angezeigt. Sie können die Eigenschaften nach Name oder Wert sortieren:<ul><li>Auf der Registerkarte <strong>Client</strong> werden Eigenschaften und Werte während des clientseitigen Teils der Installation angezeigt.</li><li>Auf der Registerkarte <strong>Server</strong> werden Eigenschaften und Werte während des Serverteils der Installation angezeigt.</li><li>Auf der Registerkarte <strong>Geschachtelt</strong> werden die Eigenschaften und Werte aller <a href="concurrent-installations.md">gleichzeitigen Installationen angezeigt.</a></li></ul> | 
| Richtlinien | Im Dialogfeld Richtlinien wird der Nach der Installation festgelegte <a href="system-policy.md">Systemrichtliniensatz</a> angezeigt:<ul><li>Der für die Richtlinie festgelegte Wert 0 (null) bedeutet, dass die Richtlinie nicht aktiviert ist.</li><li>Der Wert 1 (eins) bedeutet, dass die Richtlinie aktiviert ist.</li><li>Der Wert ? (Fragezeichen) bedeutet, dass der Richtlinienwert nicht im Protokoll aufgezeichnet wird.</li></ul>Wenn Sie einen Richtlinienwert benötigen, der nicht im Protokoll enthalten ist, verwenden Sie Regedit.exe, um die Registrierungsschlüssel auf dem Computer zu überprüfen, auf dem die Installation fehlschlägt.<br /> | 




 

## <a name="report-files"></a>Berichtsdateien

Wenn Sie eine Analyse im stillen Modus durchführen oder im Dialogfeld **Detaillierte Protokolldateiansicht** auf die Schaltfläche **Ergebnisse speichern** klicken, generiert das tool Windows Installer Setup Analyzer drei Textdateien und eine MIT HTML-Anmerkungen versehene Protokolldatei.

In der folgenden Tabelle sind die Namen und Inhalte in den Berichtsdateien aufgeführt.



| Name                      | BESCHREIBUNG                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| protokolldateiname \_summary.txt  | Fasst die Protokolldatei zusammen. Listet die Informationen, die im Dialogfeld Detaillierte Protokolldateiansicht angezeigt werden, und den ersten Fehler auf.         |
| protokolldateiname \_errors.txt   | Identifiziert die Anzahl der Fehler, die Fehler und die empfohlenen Lösungen. Diese Datei listet sowohl kritische als auch nicht kritische Fehler auf. |
| protokolldateiname \_policies.txt | Identifiziert die Richtliniennamen und -werte, die am Ende der Installation festgelegt sind, wie im Dialogfeld Richtlinien.                       |
| Details \_logfilename.htm  | Ein HTML-Protokoll mit Anmerkungen mit einer Legende für die Farbcodierung.                                                                      |



 

## <a name="return-values"></a>Rückgabewerte

Wenn ungültige Befehlszeilenargumente für Vorgänge im stillen Modus übergeben werden, führt Wilogutl.exe nichts aus, und der Prozess gibt einen der Werte in der folgenden Tabelle zurück.



| Wert | Bedeutung                                                                 |
|-------|-------------------------------------------------------------------------|
| 1     | Ungültiges Ausgabeverzeichnis wird angegeben.                                      |
| 2     | Ungültiger Protokolldateiname wird angegeben.                                         |
| 3     | /q wurde übergeben, aber es fehlt der erforderliche Schalter /l für den Protokolldateinamen. |
| 4     | /l wurde übergeben, aber es fehlt der erforderliche Schalter /q für den stillen Modus.        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Windows Installationsentwicklungstools](windows-installer-development-tools.md)
</dt> </dl>

 

 




