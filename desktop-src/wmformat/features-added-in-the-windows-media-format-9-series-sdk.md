---
title: Features, die im Windows Media Format 9 Series SDK hinzugefügt wurden
description: Features, die im Windows Media Format 9 Series SDK hinzugefügt wurden
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows Medienformat-SDK, Features
- Windows Medienformat-SDK, neue Features
- Windows Medienformat-SDK, synchrone Reader
- Windows Medienformat-SDK, framebasierte Indizierung
- Windows Medienformat-SDK, SMPTE-Zeitcodes
- Windows Medienformat-SDK, DirectShow-Filter
- Windows Medienformat-SDK, DRM-Schreibfunktion
- Windows Medienformat-SDK, Dateisenken
- Windows Medienformat-SDK, DirectX-Videobeschleunigung (DXVA)
- Windows Medienformat-SDK, Multichannel-Audio
- Windows Medienformat-SDK, Wasserzeichen
- Windows Medienformat-SDK, Unterstützung mehrerer Sprachen
- Windows Medienformat-SDK, Gerätekonformitätsvorlagen
- Windows Medienformat-SDK, Codecenumerationen
- Windows Medienformat-SDK, gegenseitiger Ausschluss
- Windows Medienformat-SDK, Mehrfachbitrate (MBR)
- Windows Medienformat-SDK,Transcodierung mit intelligenter Neukomprimierung
- Windows Medienformat-SDK, intelligente Neukomprimierung
- Windows Medienformat-SDK, Neukomprimierung
- Windows Medienformat-SDK, Metadaten
- Windows Medienformat-SDK, dynamisches Pixel-Seitenverhältnis
- Windows Medienformat-SDK, geschachtelte Videostreams
- Windows Medienformat-SDK, Zwei-Pass-Codierung
- Windows Media Format SDK,WMStub.lib
- synchrone Reader, Informationen
- framebasierte Indizierung
- SMPTE-Zeitcodes,Informationen
- DirectShow-Filter
- Dateisenken, Erweiterungen
- Multichannelaudio, Informationen
- Wasserzeichen, Informationen
- Codecs, Enumerationen
- gegenseitiger Ausschluss,Informationen
- Digital Rights Management (DRM), Schreibfunktion
- DRM (Digital Rights Management), Schreibfunktion
- DirectX-Videobeschleunigung (DXVA), Informationen
- DXVA (DirectX-Videobeschleunigung),Informationen
- Advanced Systems Format (ASF), Unterstützung mehrerer Sprachen
- ASF (Advanced Systems Format), Unterstützung mehrerer Sprachen
- Multiple Bit Rate (MBR),About
- MBR (Multiple-Bit-Rate),Informationen
- Transcodierung mit intelligenter Neukomprimierung
- Intelligente Neukomprimierung
- Neukomprimierung
- metadata,Windows Media Format SDK
- Dynamisches Pixel-Seitenverhältnis
- Videostreams mit Interlacing
- Zwei-Pass-Codierung, Informationen
- 2-Pass-Codierung, Informationen
- WMStub.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76dc0f4a8c0b23ba33409039ae7f1d46ada1b3299790ef82fb98b8714f616117
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547450"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a>Features, die im Windows Media Format 9 Series SDK hinzugefügt wurden

Das Windows Media Format 9 Series SDK hat viele Verbesserungen und Features eingeführt. Dieser Abschnitt bietet eine Übersicht über diese Features, die den Vorteil haben, dass Benutzer von einer früheren Version des SDK migrieren.

## <a name="synchronous-reading"></a>Synchrones Lesen

Sie können ASF-Dateien mit synchronen Aufrufen lesen. Beim synchronen Lesen einer Datei können Sie die Einstellungen des Readers beim Lesen ändern. Die synchronen Lesevorgänge des SDK bieten keine Unterstützung für das Lesen von Dateien über das Internet, aber Sie können die COM-Standardschnittstelle **IStream** verwenden, um aus benutzerdefinierten Quellen zu lesen.

## <a name="frame-based-indexing"></a>Framebasierte Indizierung

Asf-Dateien können basierend auf Videoframes indiziert werden. Sowohl der Reader als auch der synchrone Reader können einen Frame eines Videostreams suchen und die anderen Streams mit diesem Frame synchronisieren.

## <a name="indexing-and-seeking-with-smpte-time-code"></a>Indizieren und Suchen mit SMPTE-Zeitcode

Mit dem Windows Media Format SDK können Sie SMPTE-Zeitcodes in ASF-Dateien speichern. Dateien können durch SMPTE-Zeitcode indiziert werden, und sowohl der asynchrone Reader als auch der synchrone Reader können nach SMPTE-Zeitcodeindexeinträgen suchen.

## <a name="directshow-filters"></a>DirectShow-Filter

Das Windows Media Format SDK enthält zwei Microsoft DirectShow®filter, mit denen DirectShow-basierte Anwendungen ASF-Dateien lesen und schreiben können. DirectShow ermöglicht es Anwendungen auch, Daten von Audiovideogeräten zu erfassen und Daten aus einer Vielzahl von Formaten zu dekomprimieren, bevor sie als medienbasierte Inhalte Windows neu codiert werden.

## <a name="enhanced-profiles"></a>Erweiterte Profile

Profile können Informationen zur Freigabe der Bandbreite und Datenstrompriorisierungsinformationen enthalten. Mithilfe der Bandbreitenfreigabe können Sie angeben, dass zwei oder mehr Datenströme unabhängig von den einzelnen Bitraten niemals mehr als eine angegebene Bandbreite verwenden. Die Bandbreitenfreigabedaten in einem Profil sind rein informationshalber. sie wird von keiner Logik im SDK erzwungen. Mit der Streampriorisierung können Sie eine Prioritätsreihenfolge für die Streams in einem Profil angeben. Wenn bei der Wiedergabe nicht genügend Bandbreite vorhanden ist, um die Datei ordnungsgemäß zu streamen, können die Streams mit der niedrigsten Priorität ignoriert werden, um die Leistung zu verbessern.

## <a name="drm-writing-capability"></a>DRM-Schreibfunktion

Zusätzlich zur vorhandenen DRM-Leseunterstützung hat das SDK der Windows Media Format 9-Serie Unterstützung für das Schreiben von ASF-Dateien mit DRM-Schutz der Version 1 oder DRM Version 7 hinzugefügt. Diese neue Funktion ermöglicht "Live-DRM"-Szenarien, z. B. Webcasting mit nutzungsbasierter Bezahlung von Liveereignissen oder Veranstaltungen.

## <a name="enhanced-file-sink"></a>Erweiterte Dateisenke

Der Version der 9-Serie des SDK wurden mehrere neue Dateisenkenfunktionen hinzugefügt. Sie können die Dateisenke so konfigurieren, dass die automatische Indizierung neu erstellter ASF-Dateien deaktiviert wird. Sie haben auch die Möglichkeit, sie für nicht gepufferte Eingaben und Ausgaben zu konfigurieren.

## <a name="directx-video-acceleration"></a>DirectX-Videobeschleunigung

DirectX Video Acceleration (DXVA) ist eine Technologie, die die Wiedergabe von Videos mit hoher Bitrate (DVD-Qualität oder höher) auf weniger leistungsstarken Computern mit DXVA-fähigen Grafikkarten ermöglicht. Sie können das Readerobjekt dieses SDK verwenden, um die DirectX-Videobeschleunigung beim Wiedergeben von ASF-Dateien zu aktivieren, sofern die Hardware dies unterstützt.

## <a name="multichannel-audio"></a>Multichannelaudio

Sie können Multichannel-Audio codieren und wiedergeben. Der Windows Media Audio 9 Professional Codec unterstützt Formate mit 6 Kanälen und 8 Kanälen sowie High Definition Stereo.

## <a name="watermarking"></a>Wasserzeichen

Sie können ASF-Dateien aus Sicherheitsgründen mit digitalen Wasserzeichen codieren. Alle Wasserzeichensysteme unterscheiden sich in ihrem Ansatz, aber alle betten die Identifikation in codierten Inhalt ein. Das Wasserzeichen wird mithilfe spezieller DirectX®-Medienobjekte (DMOs) von Drittanbietern ausgeführt.

## <a name="support-for-multiple-languages-in-asf-files"></a>Unterstützung für mehrere Sprachen in ASF-Dateien

Sie können mehrere Sprachen in ASF-Dateien unterstützen, sowohl in Streams als auch in Metadaten. Beispielsweise können Sie eine Videodatei mit Audiostreams in mehreren Sprachen erstellen. Bei der Wiedergabe kann der Benutzer auswählen, welche Sprache verwendet werden soll, oder Ihre Anwendung kann die Systeminformationen auf dem wiedergabenden Computer abfragen und automatisch eine Sprache auswählen. Metadatenattribute können auch mehrmals eingegeben werden, wobei die Werte in verschiedenen Sprachen vorliegen.

## <a name="device-conformance-templates"></a>Gerätekonformitätsvorlagen

Um die Ausrichtung von Inhalten auf bestimmte Clientgeräte zu unterstützen, unterstützen die Windows Mediencodecs jetzt Gerätekonformitätsvorlagen. Jede Vorlage enthält einen definierten Bereich von Einstellungen und Codecfunktionen, die für Medien verwendet werden sollen, die für eine bestimmte Kategorie von Plattformen vorgesehen sind. Systemprofile werden mit den neuesten Versionen der Windows Mediencodecs nicht mehr unterstützt. Alle Profile müssen ihren Anforderungen entsprechend angepasst werden. Sie können Gerätekonformitätsvorlagen verwenden, um Sie beim Entwerfen Ihrer Profile zu unterstützen.

## <a name="expanded-codec-enumeration"></a>Erweiterte Codecenumeration

Das Profil-Manager-Objekt kann die Windows Medienaudio- und Videocodecs nach unterstützten Formaten abfragen. Sie können Parameter für die abgerufenen Formate festlegen. Beispielsweise können Sie alle qualitätsbasierten Formate mit variabler Bitrate abrufen, die vom Windows Media Audio 9-Codec unterstützt werden.

## <a name="improved-mutual-exclusion"></a>Verbesserter gegenseitiger Ausschluss

Sie können benannte Datensätze erstellen, die mehrere Streams innerhalb eines gegenseitigen Ausschlussobjekts enthalten. Sie können auch gegenseitige Ausschlussobjekte benennen, um sie leichter zu identifizieren. Dadurch können Sie Ebenen des gegenseitigen Ausschlusses erstellen. Eine Datei kann z. B. Streams enthalten, die sich durch Bitrate und Sprache gegenseitig ausschließen. Der sprachbasierte gegenseitige Ausschluss würde Gruppen von Streams umfassen, die jeweils aus Streams in der gleichen Sprache bestehen, sich jedoch durch die Bitrate gegenseitig ausschließen.

## <a name="expanded-multiple-bit-rate-support"></a>Erweiterte Unterstützung der Multiple-Bit-Rate

Unterstützung für gegenseitigen Ausschluss ist für MBITR-Audio (Multiple Bit Rate) und für Videos mit Streams unterschiedlicher Bildgröße enthalten.

## <a name="attributes-for-streams"></a>Attribute für Streams

Sie können einzelnen Streams in ASF-Dateien Attribute zuweisen. Sie müssen weiterhin Attribute auf Dateiebene für MP3-Dateien verwenden. Dieses Feature fügt dem SDK keine Methoden hinzu, aber die vorhandenen Methoden akzeptieren jetzt andere Streamnummern als 0 (null).

## <a name="transcoding-with-smart-recompression"></a>Transcodieren mit smarter Rekomprimierung

Mit der intelligenten Rekomprimierung können Sie Windows Medienaudiodateien von einer hohen Bitrate in eine niedrigere Bitrate mit einer besseren Qualität als zuvor erreichbar transcodieren.

## <a name="expanded-metadata-support"></a>Erweiterte Metadatenunterstützung

Das Windows Media Format SDK bietet die folgenden neuen Metadatenfeatures:

-   Indexbasierte Metadatentags, die mehrere Tags mit demselben Namen ermöglichen.
-   Möglichkeit zum Lesen von DRM-Headerattributen ohne eine WMStubDRM.lib-Datei.
-   Attribute mit mehr als 64 KB zugeordneten Daten.
-   Attribute in mehreren Sprachen.
-   Dutzende neuer vordefinierter Attribute.

## <a name="dynamic-pixel-aspect-ratio"></a>Dynamisches Pixel-Seitenverhältnis

Videostreams, die aus verschiedenen Inhaltstypen bestehen, können berücksichtigt werden, indem das Pixel-Seitenverhältnis der unterschiedlichen Stichproben im Stream identifiziert wird. Dies ermöglicht es der Wiedergabeanwendung, eine bessere Wiedergabe solcher Inhalte zu ermöglichen.

## <a name="interlaced-video-streams"></a>Interlaced Video Streams

Frühere Versionen des Windows Media Format SDK haben die Möglichkeit [](wmformat-glossary.md) bereitgestellt, Zwischeninhalte in einen Progressive Scan-Videostream zu codieren. Ab dem Windows Media Format 9 Series SDK können Sie Interlacingvideo codieren und dabei das Interlaced-Format beibehalten. Dies kann zu einer verbesserten Wiedergabe führen, insbesondere auf Verschachtelungsgeräten wie Fernsehsendungen.

## <a name="two-pass-encoding"></a>Two-Pass Codierung

Die neuen Windows Mediencodecs ermöglichen die Zwei-Durch-Durch-Codierung. Inhalte, die in zwei Durchläufen codiert sind, können eine ausgabe mit höherer Qualität erzielen.

## <a name="new-speech-codec"></a>Neuer Sprachcodec

Dieses SDK enthält den neuen Windows Media Audio 9 Voice-Codec, der für die Codierung der menschlichen Stimme bei Verwendung einer niedrigen Bitrate optimiert ist. Dieser Codec bietet auch eine bessere Leistung für gemischten Musikstimmeninhalt.

## <a name="accessible-video-frame-duration"></a>Accessible Video Frame Duration

Sie können das Writer-Objekt dieses SDK die Dauer von Videoframes für den Reader bereitstellen lassen.

## <a name="streaming-html"></a>Streaming HTML

Mit der vorherigen Version dieses SDK konnten Sie einen Skriptbefehl verwenden, um Ihrer Anwendung zu signalisieren, eine Webseite zu öffnen. Ab dem Windows Media Format 9 Series SDK können Sie die Komponenten von Webseiten in Ihren ASF-Dateien speichern, um sicherzustellen, dass es keine Verzögerung bei Präsentationen gibt.

## <a name="wmstublib-no-longer-required-for-build-environment"></a>WMStub.lib nicht mehr für Buildumgebung erforderlich

Die Buildumgebungseinstellungen für das Windows Media Format SDK wurden ab dem Windows Media Format 9 Series SDK geändert. WmStub.lib muss für Anwendungen, die dieses SDK verwenden, nicht mehr enthalten sein. DRM-fähige Anwendungen müssen jedoch weiterhin einen separaten Lizenzvertrag und eine eindeutige statische Bibliothek von Microsoft abrufen und unterzeichnen. Wenden wmla@microsoft.com Sie sich an , um weitere Informationen zur DRM-Bibliothek und zum Lizenzvertrag zu erhalten. Weitere Informationen zum Erstellen von Projekten mit diesem SDK finden Sie unter [Bibliotheksdateien und Compiler Einstellungen](library-files-and-compiler-settings.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




