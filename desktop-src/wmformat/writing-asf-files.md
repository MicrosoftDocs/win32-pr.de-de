---
title: Schreiben von ASF-Dateien
description: Schreiben von ASF-Dateien
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows Media-Format-SDK, Schreiben von ASF-Dateien
- Windows Media-Format-SDK, Erstellen von ASF-Dateien
- Windows Media-Format-SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), Schreiben von Dateien
- ASF (Advanced Systems Format), Schreiben von Dateien
- Advanced Systems Format (ASF), Erstellen von Dateien
- ASF (Advanced Systems Format), Erstellen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c13c1af0d3699c89d26f007e00675ea563639c4e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858007"
---
# <a name="writing-asf-files"></a>Schreiben von ASF-Dateien

Sie können das Writer-Objekt des SDK für den Windows Media-Format verwenden, um ASF-Dateien aus digitalen Mediendaten zu erstellen. Um eine Instanz des Writer-Objekts zu erstellen, rufen Sie die [**wmkreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) -Funktion auf. Das Writer-Objekt koordiniert die Funktionalität einer Reihe von Komponenten, einschließlich Codecs, die für das Windows Media-Format-SDK extern sind.

Die grundlegende Funktionalität des Writer-Objekts kann in die folgenden Schritte aufgeteilt werden. In den folgenden Schritten bezieht sich "die Anwendung" auf das Programm, das Sie mit dem Windows Media-Format-SDK schreiben.

1.  Die Anwendung stellt dem Writer ein Profil zur Verfügung, das beim Erstellen der ASF-Datei verwendet werden soll. Wenn der Writer die Profildaten lädt, wird jeder Verbindung des Profils eine Eingabe Nummer zugewiesen.
2.  Die Anwendung stellt dem Writer einen Ausgabe Dateinamen für die Datei zur Verfügung, die geschrieben werden soll. Der Writer erstellt ein Writer-Datei-Sink-Objekt, um die Erstellung und Eingabe von Dateien zu verwalten. Weitere Informationen finden Sie unter [Writer File Sink Object](writer-file-sink-object.md).
3.  Der Writer erstellt basierend auf den Informationen im Profil einen Header für die neue Datei.
4.  Die Anwendung übergibt nicht komprimierte Beispiele an den Writer. Die Beispiele werden nacheinander in Puffern in Puffer Objekten übermittelt. Die Anwendung sollte die Beispiele für jeden Stream gleichzeitig übergeben, damit der Writer alle Beispiele in der Präsentationszeit Reihenfolge empfängt.
5.  Der Writer übergibt die Beispiele für die Komprimierung an den entsprechenden Codec. Wenn der Writer die komprimierten Beispiele empfängt, werden diese mit Beispielen aus den anderen Datenströmen verknüpft, sodass Beispiele unabhängig vom Stream in der Präsentationszeit Reihenfolge in die Datei gelangen. Die Beispiel Daten werden dann in Pakete erstellt und in den Daten Abschnitt der Datei geschrieben.
6.  Wenn alle Beispiele verarbeitet werden, kann der Writer der Datei einen Index hinzufügen, um die Suchleistung zu verbessern.

Diese Schritte werden unter anderem in der wmstats-Beispielanwendung veranschaulicht. Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).

Der Writer unterstützt auch erweiterte Funktionen, sodass Sie die folgenden Aufgaben ausführen können:

-   Bearbeiten Sie die Metadaten im Header der Datei.
-   Schreiben Sie vorkomprimierte Beispiele.
-   Schreiben in Netzwerk senken für das Streamen von Livedaten.
-   Schreiben in Datei senken für erweiterte Optionen für die Datei Steuerung.
-   Schreiben Sie in pushsenken für die Verteilung auf Server, die Endbenutzern Inhalte bereitstellt.
-   Übermitteln Sie Postview-Beispiele für die Überprüfung der Ausgabe.
-   Übermitteln von Writer-Leistungsstatistiken.

In den folgenden Abschnitten wird die Verwendung des Writer-Objekts ausführlich beschrieben.



| `Section`                                                                    | BESCHREIBUNG                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Verwenden von Profilen mit dem Writer](to-use-profiles-with-the-writer.md)     | Beschreibt, wie Sie ein Profil angeben, das mit dem Writer verwendet werden soll.                                             |
| [Arbeiten mit Eingaben](working-with-inputs.md)                             | Beschreibt, wie die Eingabeeinstellungen im Writer identifiziert und konfiguriert werden.                              |
| [So bearbeiten Sie Metadaten mit dem Writer](to-edit-metadata-with-the-writer.md)   | Beschreibt, wie der Writer zum Bearbeiten von Metadaten für eine neue Datei verwendet wird.                                       |
| [So schreiben Sie Beispiele](to-write-samples.md)                                   | Beschreibt, wie Beispiele an den Writer übergeben werden.                                                           |
| [Festlegen von Dateneinheiten Erweiterungen](setting-data-unit-extensions.md)           | Hier wird beschrieben, wie Sie den Beispielen erweiterte Daten hinzufügen.                                                         |
| [Schreiben von komprimierten Beispielen](writing-compressed-samples.md)               | Beschreibt, wie vorkomprimierte Beispiele an den Writer übergeben werden.                                            |
| [Schreiben von bildstreams](writing-image-streams.md)                         | Beschreibt, wie eine Eingabe für einen Bildstream konfiguriert wird.                                               |
| [Schreiben von Video Bildbeispielen](writing-video-image-samples.md)             | Beschreibt, wie Video Bildbeispiele konfiguriert werden.                                                        |
| [Schreiben von variablenbitrate-Streams](writing-variable-bit-rate-streams.md) | Beschreibt das Schreiben von Datenströmen variabler Bitrate (VBR).                                                |
| [Verwenden von Two-Pass Codierung](using-two-pass-encoding.md)                     | Beschreibt, wie der Codec einen vorläufigen Durchlauf vor dem Schreiben der Datei durchführt.                    |
| [So erzwingen Sie Key-Frame einfügen](to-force-key-frame-insertion.md)           | Beschreibt, wie der Codec manuell erzwungen wird, um ein Beispiel als Keyframe zu codieren.                           |
| [So verwalten Sie die Schreib Latenz](to-manage-writer-latency.md)                   | Beschreibt, wie Sie die Zeit minimieren, die der Writer zum Verarbeiten von Beispielen in eine Ausgabedatei oder-Senke benötigt. |
| [Arbeiten mit Writer-senken](working-with-writer-sinks.md)                 | Beschreibt die Verwendung von Writer-senken zum Übermitteln Ihrer Inhalte an Dateien oder Netzwerkspeicher Orte.               |
| [So erhalten Sie eine Writer-Statistik](to-get-writer-statistics.md)                   | Beschreibt, wie Statistiken für den Writer angezeigt werden.                                                        |
| [So verwenden Sie die Writer-Postview](to-use-writer-postview.md)                       | Beschreibt, wie nicht komprimierte Beispiele beim Schreiben einer Datei zur Überprüfung erhalten werden.                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> <dt>

[**Writer-Dateisenke (Objekt)**](writer-file-sink-object.md)
</dt> <dt>

[**Writer-netzwerksink-Objekt**](writer-network-sink-object.md)
</dt> <dt>

[**Writer-Objekt**](writer-object.md)
</dt> </dl>

 

 




