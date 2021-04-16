---
title: Klassifizierungen von MCI-Befehlen
description: Klassifizierungen von MCI-Befehlen
ms.assetid: e03edfab-06c9-4337-935b-9effd2996c2e
keywords:
- MCI-Befehle, Klassifizierungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1524e6aa2094679e91acddb9dbfbb8cb480eb39f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515507"
---
# <a name="classifications-of-mci-commands"></a>Klassifizierungen von MCI-Befehlen

MCI definiert vier Befehls Klassifizierungen: "System", "required", "Basic" und "Extended". Diese Befehls Klassifizierungen werden in der folgenden Liste beschrieben:

-   *System Befehle* werden von MCI direkt und nicht vom Treiber verarbeitet.
-   *Erforderliche Befehle* werden vom Treiber verarbeitet. Alle MCI-Treiber müssen die erforderlichen Befehle und Flags unterstützen.
-   *Grundlegende Befehle* (oder optionale Befehle) werden von einigen Geräten verwendet. Wenn ein Gerät einen grundlegenden Befehl unterstützt, muss es einen definierten Satz von Flags für diesen Befehl unterstützen.
-   *Erweiterte Befehle* sind spezifisch für einen Gerätetyp oder Treiber. Erweiterte Befehle enthalten Befehle, wie z. b. die Befehle [**Put**](put.md) ([**MCI \_ Put**](mci-put.md)) und [**Where**](where.md) ([**MCI \_ Where**](mci-where.md)) für die **Digitalvideo** -und **Overlay** -Gerätetypen sowie Erweiterungen für vorhandene Befehle (z. b. das Flag "Stretch" des [**Status**](status.md) ([**MCI- \_ Status**](mci-status.md)) für den überlagerungstyp).

Während System-und erforderliche Befehle den minimalen Befehlssatz für jeden MCI-Treiber sind, werden die grundlegenden und erweiterten Befehle nicht von allen Treibern unterstützt. Die Anwendung kann immer System-und erforderliche Befehle und ihre Flags verwenden. Wenn Sie jedoch einen einfachen oder erweiterten Befehl oder ein Flag verwenden muss, sollte der Treiber zuerst mithilfe des Befehls " [**Capability**](capability.md) " ([**MCI \_ getdevcaps**](mci-getdevcaps.md)) abgefragt werden. In den folgenden Abschnitten werden die spezifischen Befehle in den einzelnen Kategorien zusammengefasst.

## <a name="system-commands"></a>System Befehle

MCI verarbeitet die folgenden Systembefehle direkt, anstatt Sie an MCI-Geräte zu übergeben.



| String                 | `Message`                             | BESCHREIBUNG                            |
|------------------------|-------------------------------------|----------------------------------------|
| [**Umbruch**](break.md) | [**MCI-unter \_ Brechung**](mci-break.md)     | Legt einen Break-Schlüssel für ein MCI-Gerät fest.    |
| [sysinfo](sysinfo.md) | [**MCI- \_ sysinfo**](mci-sysinfo.md) | Gibt Informationen zu MCI-Geräten zurück. |



 

## <a name="required-commands"></a>Erforderliche Befehle

Alle MCI-Geräte unterstützen die folgenden erforderlichen Befehle.



| String                           | `Message`                                   | BESCHREIBUNG                                                                                                               |
|----------------------------------|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Re**](capability.md) | [**MCI- \_ getdevcaps**](mci-getdevcaps.md) | Ruft die Funktionen eines Geräts ab.                                                                                     |
| [**ihrer**](close.md)           | [**MCI- \_ Schließen**](mci-close.md)           | Schließt das Gerät.                                                                                                        |
| [**Opo**](info.md)             | [**MCI- \_ Informationen**](mci-info.md)             | Ruft Textinformationen von einem Gerät ab.                                                                                |
| [**eren**](open.md)             | [**MCI \_ geöffnet**](mci-open.md)             | Initialisiert das Gerät.                                                                                                   |
| [**status**](status.md)         | [**MCI- \_ Status**](mci-status.md)         | Ruft Statusinformationen vom Gerät ab. Einige dieser Befehlsflags sind nicht erforderlich, daher ist es auch ein grundlegender Befehl. |



 

Geräte müssen auch einen Standardsatz von Befehlsflags für die erforderlichen Befehle unterstützen.

## <a name="basic-commands"></a>Grundlegende Befehle

In der folgenden Liste sind die grundlegenden Befehle zusammengefasst. Die Verwendung dieser Befehle durch ein MCI-Gerät ist optional.



| String                   | `Message`                           | BESCHREIBUNG                                                                                                                                                                                                                             |
|--------------------------|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Laden**](load.md)     | [**MCI- \_ Auslastung**](mci-load.md)     | Lädt Daten aus einer Datei.                                                                                                                                                                                                                 |
| [**Brechung**](pause.md)   | [**MCI- \_ Pause**](mci-pause.md)   | Beendet die Wiedergabe. Die Wiedergabe oder Aufzeichnung kann an der aktuellen Position fortgesetzt werden.                                                                                                                                                            |
| [**Theater**](play.md)     | [**MCI- \_ Play**](mci-play.md)     | Startet das Übertragen von Ausgabedaten.                                                                                                                                                                                                        |
| [**Aufnahme**](record.md) | [**MCI- \_ Datensatz**](mci-record.md) | Startet die Aufzeichnung von Eingabedaten.                                                                                                                                                                                                            |
| [**zusetzen**](resume.md) | [**MCI-Fortsetzung \_**](mci-resume.md) | Nimmt die Wiedergabe oder Aufzeichnung auf einem angehaltenen Gerät wieder auf.                                                                                                                                                                                        |
| [**sicher**](save.md)     | [**MCI- \_ Speicherung**](mci-save.md)     | Speichert Daten in einer Datenträger Datei.                                                                                                                                                                                                              |
| [**einzuholen**](seek.md)     | [**MCI- \_ Suche**](mci-seek.md)     | Sucht vorwärts oder rückwärts.                                                                                                                                                                                                              |
| [**Set**](set.md)       | [**MCI- \_ Gruppe**](mci-set.md)       | Legt den Betriebszustand des Geräts fest.                                                                                                                                                                                                 |
| [**status**](status.md) | [**MCI-Status**](mci-status.md)  | Ruft Statusinformationen zum Gerät ab. Dies ist auch ein erforderlicher Befehl. Da einige ihrer Flags nicht erforderlich sind, werden Sie hier ebenfalls aufgeführt. (Die optionalen Elemente unterstützen Geräte, die lineare Medien mit identifizierbaren Positionen verwenden.) |
| [**anzuhalten**](stop.md)     | [**MCI- \_ Beendigung**](mci-stop.md)     | Beendet die Wiedergabe.                                                                                                                                                                                                                          |



 

Wenn ein Treiber einen grundlegenden Befehl unterstützt, muss er auch einen Standardsatz von Flags für den Befehl unterstützen.

## <a name="extended-commands"></a>Erweiterte Befehle

Einige MCI-Geräte verfügen über zusätzliche Befehle, oder Sie fügen den vorhandenen Befehlen Flags hinzu. Einige erweiterte Befehle gelten nur für einen bestimmten Gerätetreiber, die meisten gelten jedoch für alle Treiber eines bestimmten Gerätetyps. Beispielsweise erweitert der Befehlssatz für den **Sequencer** -Gerätetyp den [**set**](set.md) ([**MCI \_ Set**](mci-set.md))-Befehl, um Zeitformate hinzuzufügen, die von den MIDI-Sequencern benötigt werden.

Sie sollten nicht davon ausgehen, dass das Gerät die erweiterten Befehle oder Flags unterstützt. Sie [**können den Funktions**](capability.md) Befehl ([**MCI \_ getdevcaps**](mci-getdevcaps.md)) verwenden, um zu bestimmen, ob ein bestimmtes Feature unterstützt wird, und Ihre Anwendung sollte bereit sein, die Rückgabewerte "nicht unterstützter Befehl" oder "nicht unterstützte Funktion" zu behandeln.

Die folgenden erweiterten Befehle sind mit den aufgelisteten Gerätetypen verfügbar.



| String                         | `Message`                                 | Device types (Gerätetypen)            | BESCHREIBUNG                                                                                       |
|--------------------------------|-----------------------------------------|-------------------------|---------------------------------------------------------------------------------------------------|
| [**Konfigurieren**](configure.md) | [**MCI- \_ Konfiguration**](mci-configure.md) | Digitalvideo            | Zeigt ein Konfigurations Dialogfeld an.                                                              |
| [**STI**](cue.md)             | [**MCI \_ -Hinweis**](mci-cue.md)             | Digitalvideo, waveaudiodatei | Bereitet die Wiedergabe oder Aufzeichnung vor.                                                                |
| [**delete**](delete.md)       | [**MCI \_ Löschen**](mci-delete.md)       | waveaudiodatei               | Löscht ein Daten Segment aus der Mediendatei.                                                       |
| [Weg](escape.md)           | [**MCI- \_ Escape**](mci-escape.md)       | Videodisk               | Sendet benutzerdefinierte Informationen an ein Gerät.                                                             |
| [**ge**](freeze.md)       | [**MCI- \_ Einfrieren**](mci-freeze.md)       | overlay                 | Deaktiviert die Video Erfassung für den Frame Puffer.                                                   |
| [**stellte**](put.md)             | [**MCI-Put**](mci-put.md)              | Digitalvideo, Overlay   | Definiert das Quell-, Ziel-und Rahmen Fenster.                                               |
| [**erkannten**](realize.md)     | [**MCI- \_ Umsetzung**](mci-realize.md)     | Digitalvideo            | Weist das Gerät an, seine Palette in einem Gerätekontext des angezeigten Fensters auszuwählen und zu erkennen. |
| [**setaudiodatei**](setaudio.md)   | [**MCI \_ -setaudiodatei**](mci-setaudio.md)  | Digitalvideo            | Legt Audioparameter für Videos fest.                                                                  |
| [**setvideo**](setvideo.md)   | [**MCI- \_ setvideo**](mci-setvideo.md)  | Digitalvideo            | Legt Video Parameter fest.                                                                            |
| [**aussendet**](signal.md)       | [**MCI- \_ Signal**](mci-signal.md)       | Digitalvideo            | Identifiziert eine angegebene Position mit einem Signal.                                                    |
| [**Spirale**](spin.md)           | [**MCI- \_ Spin**](mci-spin.md)           | Videodisk               | Startet das Drehen der CD oder hält die Scheibe an.                                         |
| [**Schritt**](step.md)           | [**MCI- \_ Schritt**](mci-step.md)           | Digitalvideo, Videodisk | Schritte zum Wiedergeben eines oder mehrerer Frames vor-oder rückgängig.                                             |
| [**Fixierung aufheben**](unfreeze.md)   | [**MCI- \_ Sperrung aufheben**](mci-unfreeze.md)   | overlay                 | Ermöglicht dem Frame Puffer das Abrufen von Videodaten.                                                   |
| [**alisierungs**](update.md)       | [**MCI- \_ Update**](mci-update.md)       | Digitalvideo            | Zeichnet den aktuellen Frame in den Gerätekontext.                                               |
| [**Was**](where.md)         | [**MCI, wobei**](mci-where.md)          | Digitalvideo, Overlay   | Ruft das Rechteck ab, das die Quelle, das Ziel oder den Frame Bereich angibt.                          |
| [**ster**](window.md)       | [**MCI- \_ Fenster**](mci-window.md)       | Digitalvideo, Overlay   | Steuert das Anzeige Fenster.                                                                      |



 

 

 




