---
title: Features, die im SDK der Windows Media-Serie 9 hinzugefügt werden
description: Features, die im SDK der Windows Media-Serie 9 hinzugefügt werden
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows Media-Format-SDK, Features
- Windows Media-Format-SDK, neue Funktionen
- SDK für den Windows Media-Format, synchrone Reader
- Windows Media-Format-SDK, Frame basierte Indizierung
- Windows Media-Format-SDK, SMPTE-Zeit Codes
- Windows Media-Format-SDK, DirectShow-Filter
- Windows Media-Format-SDK, DRM-Schreibfunktion
- Windows Media-Format-SDK, Datei senken
- Windows Media-Format-SDK, DirectX-Video Beschleunigung (DXVA)
- Windows Media-Format-SDK, Multichannel-Audiodatei
- Windows Media-Format-SDK, Wasserzeichen
- Windows Media-Format-SDK, Unterstützung mehrerer Sprachen
- Windows Media-Format-SDK, Geräte Konformitäts Vorlagen
- Windows Media-Format-SDK, Codec-Enumerationen
- Windows Media-Format-SDK, gegenseitiger Ausschluss
- Windows Media-Format-SDK, mehrfache Bitrate (MBR)
- Windows Media-Format-SDK, Transcoding mit intelligenter Neukomprimierung
- Windows Media-Format-SDK, intelligente Neukomprimierung
- SDK für Windows Media-Format, Neukomprimierung
- SDK für Windows Media-Format, Metadaten
- Windows Media-Format-SDK, dynamisches Pixel Seitenverhältnis
- Windows Media-Format-SDK, Text Ströme mit Zeilen Sprung
- Windows Media-Format-SDK, Two-Pass-Codierung
- Windows Media-Format-SDK, wmstub. lib
- synchrone Leser, Informationen zu
- Frame basierte Indizierung
- SMPTE-Zeit Codes, Informationen zu
- DirectShow-Filter
- Datei senken, Erweiterungen
- Multichannel-Audioinformationen, Informationen zu
- Wasserzeichen, Info
- Codecs, Enumerationen
- gegenseitiger Ausschluss, Informationen
- Digital Rights Management (DRM), Schreiben von Funktionen
- DRM (Digital Rights Management), Schreiben von Funktionen
- DirectX-Video Beschleunigung (DXVA), Informationen zu
- DXVA (DirectX-Video Beschleunigung), Informationen zu
- Advanced Systems Format (ASF), Unterstützung mehrerer Sprachen
- ASF (Advanced Systems Format), Unterstützung mehrerer Sprachen
- mehrfache Bitrate (MBR), Informationen zu
- MBR (mehrfache Bitrate), Informationen zu
- Transcodierung mit intelligenter Neukomprimierung
- intelligente Neukomprimierung
- Neukomprimierung
- Metadaten, Windows Media-Format-SDK
- Verhältnis des dynamischen Pixel Aspekts
- Videodaten Ströme mit Zeilen Sprung
- zwei-Pass-Codierung, Informationen
- '2: Codierung, Informationen'
- Wmstub. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca7e39c89220c2c8c4cac6af354eefb77257aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206820"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a>Features, die im SDK der Windows Media-Serie 9 hinzugefügt werden

Das Windows Media Format 9 Series SDK hat viele Verbesserungen und Features eingeführt. Dieser Abschnitt bietet eine Übersicht über die Features, die Benutzer bei der Migration von einer früheren Version des SDK nutzen.

## <a name="synchronous-reading"></a>Synchrones lesen

Sie können ASF-Dateien mit synchronen Aufrufen lesen. Beim synchronen Lesen einer Datei können Sie die Einstellungen des Readers beim Lesen ändern. Die synchronen Lesevorgänge des SDK bieten keine Unterstützung für das Lesen von Dateien über das Internet, aber Sie können die Standard-COM-Schnittstelle **IStream** verwenden, um aus benutzerdefinierten Quellen zu lesen.

## <a name="frame-based-indexing"></a>Frame basierte Indizierung

Sie können ASF-Dateien auf der Grundlage von Video Frames indizieren. Sowohl der Reader als auch der synchrone Reader können einen Frame eines Videodaten Stroms suchen und die anderen Streams mit diesem Frame synchronisieren.

## <a name="indexing-and-seeking-with-smpte-time-code"></a>Indizierung und Suche mit SMPTE-Zeit Code

Mit dem Windows Media-Format-SDK können Sie SMPTE-Zeit Codes in ASF-Dateien speichern. Dateien können mithilfe von SMPTE-Zeit Code indiziert werden, und sowohl der asynchrone Reader als auch der synchrone Reader können nach SMPTE-Zeit Code Indexeinträgen suchen.

## <a name="directshow-filters"></a>DirectShow-Filter

Das Windows Media-Format SDK enthält zwei Microsoft DirectShow-® Filter, mit denen DirectShow-basierte Anwendungen die Möglichkeit haben, ASF-Dateien zu lesen und zu schreiben. Mithilfe von DirectShow können Anwendungen auch Daten von audiovideogeräten erfassen und Daten aus verschiedenen Formaten dekomprimieren, bevor Sie Sie als Windows Media-basierte Inhalte neu codieren.

## <a name="enhanced-profiles"></a>Erweiterte profile

Profile können Informationen zur Bandbreiten Freigabe und Informationen zur streampriorisierung enthalten. Mit der Bandbreiten Freigabe können Sie angeben, dass für zwei oder mehr Datenströme unabhängig von den einzelnen Bitraten niemals mehr als eine angegebene Bandbreite verwendet werden soll. Die Bandbreiten Freigabe von Daten in einem Profil ist nur eine Informations Meldung. Sie wird von keiner Logik im SDK erzwungen. Mithilfe der streampriorisierung können Sie eine Prioritäts Priorität für die Datenströme in einem Profil angeben. Wenn bei der Wiedergabe nicht genügend Bandbreite vorhanden ist, um die Datei ordnungsgemäß zu streamen, können Datenströme mit niedrigster Priorität ignoriert werden, um die Leistung zu verbessern

## <a name="drm-writing-capability"></a>DRM-Schreibfunktion

Zusätzlich zu der vorhandenen Unterstützung für DRM-Lesevorgänge hat das Windows Media Format 9-Serie-SDK Unterstützung für das Schreiben von ASF-Dateien mit DRM-Version 1 oder DRM-Schutz Version 7 hinzugefügt. Diese neue Funktion ermöglicht "Live DRM-Szenarien", wie z. b. Pay-per-View-Webcasting von Live Sportveranstaltungen oder Konzerten.

## <a name="enhanced-file-sink"></a>Erweiterte Datei Senke

Der 9-Serienversion des SDK wurden mehrere neue dateisenke-Funktionen hinzugefügt. Sie können die Datei Senke so konfigurieren, dass die automatische Indizierung neu erstellter ASF-Dateien deaktiviert wird. Sie haben auch die Möglichkeit, Sie für nicht gepufferte Eingaben und Ausgaben zu konfigurieren.

## <a name="directx-video-acceleration"></a>DirectX-Video Beschleunigung

Bei DirectX Video Acceleration (DXVA) handelt es sich um eine Technologie, die die Wiedergabe von Videos mit hoher Bitrate (DVD-Qualität oder besser) auf weniger leistungsfähigen Computern mit DXVA-fähigen Grafikkarten ermöglicht. Sie können das Reader-Objekt dieses SDK verwenden, um die DirectX-Video Beschleunigung bei der Wiedergabe von ASF-Dateien zu aktivieren, wenn die Hardware dies unterstützt.

## <a name="multichannel-audio"></a>Multichannel-Audiodatei

Sie können Multichannel-audiocode codieren und wiedergeben. Der Windows Media Audio 9 Professional-Codec unterstützt Formate mit 6 Kanälen und acht Kanälen sowie eine Stereo-High-Definition.

## <a name="watermarking"></a>Grenzwerte

Sie können ASF-Dateien mit digitalen Wasserzeichen für die Sicherheit codieren. Alle Wasserzeichen Systeme unterscheiden sich in ihrem Ansatz, aber alle Betten die Identifizierung in codierten Inhalt ein. Das Wasserzeichen wird mithilfe spezieller DirectX® Media Objects (DMOs) von Drittanbietern ausgeführt.

## <a name="support-for-multiple-languages-in-asf-files"></a>Unterstützung für mehrere Sprachen in ASF-Dateien

Sie können mehrere Sprachen in ASF-Dateien sowohl in Streams als auch in Metadaten unterstützen. Beispielsweise können Sie eine Videodatei mit Audiodatenströmen in verschiedenen Sprachen erstellen. Bei der Wiedergabe kann der Benutzer auswählen, welche Sprache verwendet werden soll, oder die Anwendung kann die Systeminformationen auf dem wiedergegebenen Computer Abfragen und automatisch eine Sprache auswählen. Metadatenattribute können auch mehrmals eingegeben werden, mit den Werten in verschiedenen Sprachen.

## <a name="device-conformance-templates"></a>Geräte Konformitäts Vorlagen

Zur Unterstützung bei der Ausrichtung von Inhalten auf bestimmte Client Geräte unterstützen die Windows Media-Codecs nun Geräte Konformitäts Vorlagen. Jede Vorlage enthält einen definierten Bereich von Einstellungen und Codec-Funktionen, die für Medien verwendet werden sollen, die für eine bestimmte Platt Form Plattform gedacht sind. System Profile werden in den neuesten Versionen der Windows Media-Codecs nicht mehr unterstützt. Alle Profile müssen Ihren Anforderungen entsprechend angepasst werden. Sie können Geräte Konformitäts Vorlagen verwenden, um Sie beim Entwerfen von Profilen zu unterstützen.

## <a name="expanded-codec-enumeration"></a>Erweiterte Codec-Enumeration

Das Profil-Manager-Objekt kann die Windows Media Audio und Video Codecs nach unterstützten Formaten Abfragen. Sie können Parameter für die abgerufenen Formate festlegen. Beispielsweise können Sie alle Qualitäts basierten Variablen Bitrate-Formate abrufen, die vom Windows Media Audio 9-Codec unterstützt werden.

## <a name="improved-mutual-exclusion"></a>Verbesserter gegenseitiger Ausschluss

Sie können benannte Datensätze erstellen, die mehrere Datenströme innerhalb eines gegenseitigen Ausschluss Objekts enthalten. Sie können auch Objekte für die gegenseitige Ausschluss benennen, um Sie leichter zu identifizieren. Dies ermöglicht Ihnen das Erstellen von Ebenen des gegenseitigen Ausschlusses. Eine Datei kann z. b. Datenströme enthalten, die sich nach Bitrate und Sprache gegenseitig ausschließen. Der sprachbasierte gegenseitige Ausschluss umfasst Gruppen von Streams, jede Gruppe, die aus Streams in derselben Sprache besteht, aber sich gegenseitig von der Bitrate ausschließen.

## <a name="expanded-multiple-bit-rate-support"></a>Erweiterte Unterstützung für mehrere Bitraten

Die Unterstützung gegenseitiger Ausschluss ist für MBR-Audiodaten (Multiple Bitrate) und für Videos mit unterschiedlichen Bildgrößen enthalten.

## <a name="attributes-for-streams"></a>Attribute für Streams

Sie können einzelnen Streams in ASF-Dateien Attribute zuweisen. Sie müssen weiterhin Attribute auf Dateiebene für MP3-Dateien verwenden. Diese Funktion fügt dem SDK keine Methoden hinzu, aber die vorhandenen Methoden akzeptieren jetzt streamnummern außer 0 (null).

## <a name="transcoding-with-smart-recompression"></a>Transcoding mit intelligenter Neukomprimierung

Die intelligente Neukomprimierung ermöglicht es Ihnen, Windows Media-Audiodateien von einer hohen Bitrate in eine niedrigere Bitrate zu transcodieren, die eine bessere Qualität als zuvor erreicht hat.

## <a name="expanded-metadata-support"></a>Erweiterte Metadatenunterstützung

Das Windows Media-Format SDK bietet die folgenden neuen Metadatenfeatures:

-   Index basierte Metadatentags, die mehrere Tags mit dem gleichen Namen ermöglichen.
-   Möglichkeit zum Lesen von DRM-Header Attributen ohne wmstubdrm. lib-Datei.
-   Attribute mit mehr als 64 Kilobyte zugeordneten Daten.
-   Attribute in mehreren Sprachen.
-   Dutzende von neuen vordefinierten Attributen.

## <a name="dynamic-pixel-aspect-ratio"></a>Verhältnis des dynamischen Pixel Aspekts

Videostreams, die aus verschiedenen Inhaltstypen bestehen, können durch die Identifizierung des Pixel Seitenverhältnisses der unterschiedlichen Stichproben im Stream untersucht werden. Dadurch kann die Spiele Anwendung eine bessere Wiedergabe solcher Inhalte bereitstellen.

## <a name="interlaced-video-streams"></a>Video Datenströme mit Zeilen Sprung

In früheren Versionen des SDK für den Windows Media-Format haben Sie die Möglichkeit bereitgestellt, Zeilen Sprung Inhalte in einen Videodaten Strom mit progressivem Scannen [*zu codieren*](wmformat-glossary.md) . Beginnend mit dem Windows Media Format 9-Reihe-SDK können Sie Zeilen Sprung Video codieren, während das Zeilen Sprung Format beibehalten wird. Dies kann zu einer verbesserten Wiedergabe führen, insbesondere auf Zeilen Sprung Geräten, z. b. Fernseh Sets.

## <a name="two-pass-encoding"></a>Two-Pass Codierung

Die neuen Windows Media-Codecs ermöglichen die zwei-Pass-Codierung. Inhalt, der in zwei Durchläufen codiert ist, kann eine höhere Qualität ausgeben

## <a name="new-speech-codec"></a>Neuer Sprachcodec

Dieses SDK enthält den neuen Windows Media Audio 9-Sprachcodec, der für die Codierung der menschlichen Stimme bei niedriger Bitrate optimiert ist. Dieser Codec bietet auch eine bessere Leistung für gemischte Musikinhalte.

## <a name="accessible-video-frame-duration"></a>Barrierefreie Video Frame Dauer

Sie können das Writer-Objekt dieses SDK zum Bereitstellen der Dauer von Video Frames für den Reader bereitstellen.

## <a name="streaming-html"></a>Streaming-HTML

Mit der vorherigen Version dieses SDK konnten Sie einen Skript Befehl verwenden, um Ihrer Anwendung das Öffnen einer Webseite zu signalisieren. Beginnend mit dem Windows Media Format 9-Reihe-SDK können Sie die Komponenten von Webseiten in ihren ASF-Dateien speichern, um sicherzustellen, dass es keine Verzögerung bei Präsentationen gibt.

## <a name="wmstublib-no-longer-required-for-build-environment"></a>"Wmstub. lib" ist für die Buildumgebung nicht mehr erforderlich.

Die buildumgebungseinstellungen für das SDK für Windows Media-Format wurden beginnend mit dem SDK für Windows Media-Serie 9 geändert. Sie müssen wmstub. lib nicht mehr für Anwendungen einschließen, die dieses SDK verwenden. Allerdings müssen DRM-fähige Anwendungen weiterhin einen separaten Lizenzvertrag abrufen und Signieren und eine eindeutige statische Bibliothek von Microsoft erhalten. Kontaktieren Sie, wmla@microsoft.com um weitere Informationen zur DRM-Bibliothek und zum Lizenzvertrag zu erhalten. Weitere Informationen zum Aufbau von Projekten mit diesem SDK finden Sie unter [Bibliotheksdateien und Compilereinstellungen](library-files-and-compiler-settings.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media-Format-SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




