---
title: Schreiben von ASF-Dateien
description: Schreiben von ASF-Dateien
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows Medienformat-SDK, Schreiben von ASF-Dateien
- Windows Medienformat-SDK, Erstellen von ASF-Dateien
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), Schreiben von Dateien
- ASF (Advanced Systems Format), Schreiben von Dateien
- Advanced Systems Format (ASF), Erstellen von Dateien
- ASF (Advanced Systems Format), Erstellen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4bec466a9f38dfedaa7e860fdc5e3eda56e0ca5fa1f1240bc18c54dfd51513
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590620"
---
# <a name="writing-asf-files"></a>Schreiben von ASF-Dateien

Sie können das Writer-Objekt des Windows Media Format SDK verwenden, um ASF-Dateien aus digitalen Mediendaten zu erstellen. Um eine Instanz des Writer-Objekts zu erstellen, rufen Sie die [**WMCreateWriter-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) auf. Das Writer-Objekt koordiniert die Funktionalität einer Reihe von Komponenten, einschließlich Codecs, die außerhalb des Windows Media Format SDK liegen.

Die grundlegende Funktionalität des Writer-Objekts kann in die folgenden Schritte aufgeschlüsselt werden. In diesen Schritten bezieht sich "die Anwendung" auf das Programm, das Sie mit dem Windows Media Format SDK schreiben.

1.  Die Anwendung stellt dem Writer ein Profil zur Verwendung beim Erstellen der ASF-Datei zur Anwendung. Wenn der Writer die Profildaten lädt, weist er jeder Verbindung des Profils eine Eingabenummer zu.
2.  Die Anwendung liefert dem Writer einen Ausgabedateinamen für die zu schreibende Datei. Der Writer erstellt ein Writerdatei-Senkenobjekt, um die Dateierstellung und -eingabe zu verwalten. Weitere Informationen finden Sie unter [Writer File Sink Object](writer-file-sink-object.md).
3.  Der Writer erstellt basierend auf den Informationen im Profil einen Header für die neue Datei.
4.  Die Anwendung übergibt unkomprimierte Beispiele an den Writer. Stichproben werden in Puffern, die in Pufferobjekten umschlossen sind, nach und nach übergeben. Die Anwendung sollte Stichproben für jeden Stream gleichzeitig übergeben, damit der Writer alle Stichproben in der Präsentationszeit erhält.
5.  Der Writer übergibt die Beispiele an den entsprechenden Codec für die Komprimierung. Wenn der Writer die komprimierten Stichproben empfängt, überlagert er sie mit Stichproben aus den anderen Datenströmen, sodass Stichproben unabhängig vom Datenstrom in der Präsentationszeit in die Datei übertragen werden. Die Beispieldaten werden dann in Pakete geschrieben und in den Datenabschnitt der Datei geschrieben.
6.  Wenn alle Beispiele verarbeitet werden, kann der Writer der Datei einen Index hinzufügen, um die Suchleistung zu verbessern.

Diese Schritte werden unter anderem in der WMStats-Beispielanwendung veranschaulicht. Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).

Der Writer unterstützt auch erweiterte Funktionen, sodass Sie Folgendes tun können:

-   Bearbeiten Sie Metadaten im Header der Datei.
-   Schreiben Sie vorkomprimierte Beispiele.
-   Schreiben in Netzwerksenken zum Streamen von Livedaten.
-   Schreiben in Dateisenken für erweiterte Dateisteuerungsoptionen.
-   Schreiben in Pushsenken für die Verteilung an Server, die Inhalte an Endbenutzer bereitstellen.
-   Stellen Sie Postview-Beispiele für die Überprüfung der Ausgabe zur Verfügung.
-   Liefern von Statistiken zur Writer-Leistung.

In den folgenden Abschnitten wird die Verwendung des Writer-Objekts ausführlich beschrieben.



| `Section`                                                                    | BESCHREIBUNG                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Verwenden von Profilen mit dem Writer](to-use-profiles-with-the-writer.md)     | Beschreibt, wie ein Profil angegeben wird, das mit dem Writer verwendet werden soll.                                             |
| [Arbeiten mit Eingaben](working-with-inputs.md)                             | Beschreibt, wie die Eingabeeinstellungen im Writer identifiziert und konfiguriert werden.                              |
| [So bearbeiten Sie Metadaten mit dem Writer](to-edit-metadata-with-the-writer.md)   | Beschreibt, wie der Writer verwendet wird, um Metadaten für eine neue Datei zu bearbeiten.                                       |
| [So schreiben Sie Beispiele](to-write-samples.md)                                   | Beschreibt, wie Beispiele an den Writer übergeben werden.                                                           |
| [Festlegen von Dateneinheitserweiterungen](setting-data-unit-extensions.md)           | Beschreibt das Hinzufügen erweiterter Daten zu Beispielen.                                                         |
| [Schreiben komprimierter Beispiele](writing-compressed-samples.md)               | Beschreibt, wie vorkomprimierte Beispiele an den Writer übergeben werden.                                            |
| [Schreiben von Streams](writing-image-streams.md)                         | Beschreibt, wie eine Eingabe für einen Bildstream konfiguriert wird.                                               |
| [Schreiben von Videobildbeispielen](writing-video-image-samples.md)             | Beschreibt, wie Videobildbeispiele konfiguriert werden.                                                        |
| [Schreiben variabler Bitraten Streams](writing-variable-bit-rate-streams.md) | Beschreibt, wie VBR-Streams (Variable Bit Rate) geschrieben werden.                                                |
| [Verwenden Two-Pass Codierung](using-two-pass-encoding.md)                     | Beschreibt, wie der Codec vor dem Schreiben der Datei einen vorläufigen Durchgang ausführen muss.                    |
| [So erzwingen sie Key-Frame Einfügen](to-force-key-frame-insertion.md)           | Beschreibt, wie der Codec manuell dazu zwingen kann, ein Beispiel als Keyframe zu codieren.                           |
| [So verwalten Sie die Writerlatenz](to-manage-writer-latency.md)                   | Beschreibt, wie sie die Zeit minimieren, die der Writer benötigt, um Beispiele in eine Ausgabedatei oder Senke zu verarbeiten. |
| [Arbeiten mit Writer-Senken](working-with-writer-sinks.md)                 | Beschreibt, wie Writer-Senken verwendet werden, um Ihre Inhalte an Dateien oder Netzwerkstandorte zu liefern.               |
| [So erhalten Sie Writer-Statistiken](to-get-writer-statistics.md)                   | Beschreibt, wie Statistiken für den Writer erhalten werden.                                                        |
| [So verwenden Sie writer postview](to-use-writer-postview.md)                       | Beschreibt, wie Sie unkomprimierte Beispiele erhalten, wenn Sie eine Datei für die Überprüfung schreiben.                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> <dt>

[**Writer-Dateisenke (Objekt)**](writer-file-sink-object.md)
</dt> <dt>

[**Writer-Netzwerksenkenobjekt**](writer-network-sink-object.md)
</dt> <dt>

[**Writer-Objekt**](writer-object.md)
</dt> </dl>

 

 




