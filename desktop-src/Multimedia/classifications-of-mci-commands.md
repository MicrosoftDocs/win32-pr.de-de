---
title: Klassifizierungen von MCI-Befehlen
description: Klassifizierungen von MCI-Befehlen
ms.assetid: e03edfab-06c9-4337-935b-9effd2996c2e
keywords:
- MCI-Befehle,Klassifizierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b532c56d1cdecac50cb24b14bf4f1b51c401dd5bb2501d1c421064659f1ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807929"
---
# <a name="classifications-of-mci-commands"></a>Klassifizierungen von MCI-Befehlen

MCI definiert vier Befehlklassifizierungen: system, required, basic und extended. In der folgenden Liste werden diese Befehlklassifizierungen beschrieben:

-   *Systembefehle* werden von MCI direkt und nicht vom Treiber verarbeitet.
-   *Erforderliche Befehle* werden vom Treiber verarbeitet. Alle MCI-Treiber müssen die erforderlichen Befehle und Flags unterstützen.
-   *Grundlegende Befehle* (oder optionale Befehle) werden von einigen Geräten verwendet. Wenn ein Gerät einen einfachen Befehl unterstützt, muss es einen definierten Satz von Flags für diesen Befehl unterstützen.
-   *Erweiterte Befehle* sind spezifisch für einen Gerätetyp oder Treiber. Zu den erweiterten Befehlen gehören Befehle wie [**put**](put.md) ([**MCI \_ PUT**](mci-put.md)) und [**where**](where.md) ([**MCI \_ WHERE**](mci-where.md)) für die Gerätetypen **digitalvideo** und **overlay** sowie Erweiterungen vorhandener Befehle (z. B. das Flag "stretch" des [**Statusbefehls**](status.md) ([**MCI \_ STATUS**](mci-status.md)) für den Überlagerungsgerätetyp).

Systembefehle und erforderliche Befehle sind zwar der mindeste Befehlssatz für jeden MCI-Treiber, grundlegende und erweiterte Befehle werden jedoch nicht von allen Treibern unterstützt. Ihre Anwendung kann immer system- und erforderliche Befehle und deren Flags verwenden. Wenn sie jedoch einen einfachen oder erweiterten Befehl oder ein Flag verwenden muss, sollte sie zuerst den Treiber mithilfe des Funktionsbefehls [**(MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) abfragen. [](capability.md) In den folgenden Abschnitten werden die spezifischen Befehle in den einzelnen Kategorien zusammengefasst.

## <a name="system-commands"></a>Systembefehle

MCI verarbeitet die folgenden Systembefehle direkt, anstatt sie an MCI-Geräte zu übergeben.



| String                 | `Message`                             | BESCHREIBUNG                            |
|------------------------|-------------------------------------|----------------------------------------|
| [**Brechen**](break.md) | [**MCI \_ BREAK**](mci-break.md)     | Legt einen Halteschlüssel für ein MCI-Gerät fest.    |
| [Sysinfo](sysinfo.md) | [**MCI \_ SYSINFO**](mci-sysinfo.md) | Gibt Informationen zu MCI-Geräten zurück. |



 

## <a name="required-commands"></a>Erforderliche Befehle

Alle MCI-Geräte unterstützen die folgenden erforderlichen Befehle.



| String                           | `Message`                                   | BESCHREIBUNG                                                                                                               |
|----------------------------------|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Fähigkeit**](capability.md) | [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) | Erhält die Funktionen eines Geräts.                                                                                     |
| [**Schließen**](close.md)           | [**MCI \_ CLOSE**](mci-close.md)           | Schließt das Gerät.                                                                                                        |
| [**Informationen**](info.md)             | [**\_MCI-INFORMATIONEN**](mci-info.md)             | Erhält Textinformationen von einem Gerät.                                                                                |
| [**öffnen**](open.md)             | [**MCI \_ OPEN**](mci-open.md)             | Initialisiert das Gerät.                                                                                                   |
| [**status**](status.md)         | [**\_MCI-STATUS**](mci-status.md)         | Erhält Statusinformationen vom Gerät. Einige der Flags dieses Befehls sind nicht erforderlich, daher handelt es sich auch um einen einfachen Befehl. |



 

Geräte müssen auch einen Standardsatz von Befehlsflags für die erforderlichen Befehle unterstützen.

## <a name="basic-commands"></a>Grundlegende Befehle

In der folgenden Liste sind die grundlegenden Befehle zusammengefasst. Die Verwendung dieser Befehle durch ein MCI-Gerät ist optional.



| String                   | `Message`                           | BESCHREIBUNG                                                                                                                                                                                                                             |
|--------------------------|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Laden**](load.md)     | [**MCI \_ LOAD**](mci-load.md)     | Lädt Daten aus einer Datei.                                                                                                                                                                                                                 |
| [**pause**](pause.md)   | [**MCI \_ PAUSE**](mci-pause.md)   | Beendet die Wiedergabe. Die Wiedergabe oder Aufzeichnung kann an der aktuellen Position fortgesetzt werden.                                                                                                                                                            |
| [**Spielen**](play.md)     | [**MCI \_ PLAY**](mci-play.md)     | Beginnt mit der Übertragung von Ausgabedaten.                                                                                                                                                                                                        |
| [**Aufzeichnung**](record.md) | [**MCI \_ RECORD**](mci-record.md) | Beginnt mit der Aufzeichnung von Eingabedaten.                                                                                                                                                                                                            |
| [**Fortsetzen**](resume.md) | [**MCI \_ RESUME**](mci-resume.md) | Setzt die Wiedergabe oder Aufzeichnung auf einem angehaltenen Gerät wieder auf.                                                                                                                                                                                        |
| [**Speichern**](save.md)     | [**MCI \_ SAVE**](mci-save.md)     | Speichert Daten in einer Datenträgerdatei.                                                                                                                                                                                                              |
| [**Suchen**](seek.md)     | [**MCI \_ SEEK**](mci-seek.md)     | Sucht vorwärts oder rückwärts.                                                                                                                                                                                                              |
| [**Festgelegt**](set.md)       | [**MCI \_ SET**](mci-set.md)       | Legt den Betriebszustand des Geräts fest.                                                                                                                                                                                                 |
| [**status**](status.md) | [**MCI-STATUS**](mci-status.md)  | Erhält Statusinformationen zum Gerät. Dies ist auch ein erforderlicher Befehl. Da einige seiner Flags nicht erforderlich sind, ist es auch hier aufgeführt. (Die optionalen Elemente unterstützen Geräte, die lineare Medien mit identifizierbaren Positionen verwenden.) |
| [**Stoppen**](stop.md)     | [**MCI \_ STOP**](mci-stop.md)     | Beendet die Wiedergabe.                                                                                                                                                                                                                          |



 

Wenn ein Treiber einen einfachen Befehl unterstützt, muss er auch einen Standardsatz von Flags für den Befehl unterstützen.

## <a name="extended-commands"></a>Erweiterte Befehle

Einige MCI-Geräte verfügen über zusätzliche Befehle oder fügen vorhandenen Befehlen Flags hinzu. Während einige erweiterte Befehle nur für einen bestimmten Gerätetreiber gelten, gelten die meisten für alle Treiber eines bestimmten Gerätetyps. Der Befehlssatz für den **Sequencer-Gerätetyp** erweitert z. B. den [**Set-Befehl**](set.md) ([**MCI \_ SET**](mci-set.md)), um Zeitformate hinzuzufügen, die von DEN SEQUENCE-Sequencern benötigt werden.

Sie sollten nicht davon ausgehen, dass das Gerät die erweiterten Befehle oder Flags unterstützt. Sie können den Befehl [**capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) verwenden, um zu bestimmen, ob ein bestimmtes Feature unterstützt wird, und Ihre Anwendung sollte für die Rückgabewerte "Nicht unterstützter Befehl" oder "nicht unterstützte Funktion" bereit sein.

Die folgenden erweiterten Befehle sind mit den aufgelisteten Gerätetypen verfügbar.



| String                         | `Message`                                 | Device types (Gerätetypen)            | Beschreibung                                                                                       |
|--------------------------------|-----------------------------------------|-------------------------|---------------------------------------------------------------------------------------------------|
| [**Konfigurieren**](configure.md) | [**MCI \_ CONFIGURE**](mci-configure.md) | digitalvideo            | Zeigt ein Konfigurationsdialogfeld an.                                                              |
| [**Hinweis**](cue.md)             | [**MCI \_ CUE**](mci-cue.md)             | digitalvideo, waveaudio | Bereitet die Wiedergabe oder Aufzeichnung vor.                                                                |
| [**Löschen**](delete.md)       | [**MCI \_ DELETE**](mci-delete.md)       | Waveaudio               | Löscht ein Datensegment aus der Mediendatei.                                                       |
| [Flucht](escape.md)           | [**MCI \_ ESCAPE**](mci-escape.md)       | videodisc               | Sendet benutzerdefinierte Informationen an ein Gerät.                                                             |
| [**Einfrieren**](freeze.md)       | [**MCI \_ FREEZE**](mci-freeze.md)       | overlay                 | Deaktiviert die Videoerfassung für den Framepuffer.                                                   |
| [**put**](put.md)             | [**MCI PUT**](mci-put.md)              | digitalvideo, overlay   | Definiert die Quell-, Ziel- und Rahmenfenster.                                               |
| [**Erkennen**](realize.md)     | [**MCI \_ REALIZE**](mci-realize.md)     | digitalvideo            | Weist das Gerät an, seine Palette in einem Gerätekontext des angezeigten Fensters auszuwählen und zu realisieren. |
| [**Setaudio**](setaudio.md)   | [**MCI \_ SETAUDIO**](mci-setaudio.md)  | digitalvideo            | Legt Audioparameter für Videos fest.                                                                  |
| [**setvideo**](setvideo.md)   | [**MCI \_ SETVIDEO**](mci-setvideo.md)  | digitalvideo            | Legt Videoparameter fest.                                                                            |
| [**Signal**](signal.md)       | [**MCI \_ SIGNAL**](mci-signal.md)       | digitalvideo            | Identifiziert eine angegebene Position mit einem Signal.                                                    |
| [**drehen**](spin.md)           | [**MCI \_ SPIN**](mci-spin.md)           | videodisc               | Startet das Rotieren des Datenträgers oder beendet das Drehen des Datenträgers.                                         |
| [**Schritt**](step.md)           | [**\_MCI-SCHRITT**](mci-step.md)           | digitalvideo, videodisc | Schrittweises Ausführen eines oder mehrerer Frames nach vorn oder umgekehrt.                                             |
| [**Auftauen**](unfreeze.md)   | [**MCI \_ UNFREEZE**](mci-unfreeze.md)   | overlay                 | Aktiviert den Framepuffer zum Abrufen von Videodaten.                                                   |
| [**aktualisieren**](update.md)       | [**MCI \_ UPDATE**](mci-update.md)       | digitalvideo            | Bemalt den aktuellen Frame erneut in den Gerätekontext.                                               |
| [**Wo**](where.md)         | [**MCI WHERE**](mci-where.md)          | digitalvideo, overlay   | Ruft das Rechteck ab, das die Quelle, das Ziel oder den Rahmenbereich angibt.                          |
| [**Fenster**](window.md)       | [**\_MCI-FENSTER**](mci-window.md)       | digitalvideo, overlay   | Steuert das Anzeigefenster.                                                                      |



 

 

 




