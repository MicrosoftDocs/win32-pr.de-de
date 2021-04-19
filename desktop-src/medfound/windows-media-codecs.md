---
description: Die Windows Media Audio-und Video Codecs sind eine Auflistung von Objekten, die Sie verwenden können, um digitale Mediendaten zu komprimieren und zu komprimieren.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Windows Media-Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106353636"
---
# <a name="windows-media-codecs"></a>Windows Media-Codecs

Die Windows Media Audio-und Video Codecs sind eine Auflistung von Objekten, die Sie verwenden können, um digitale Mediendaten zu komprimieren und zu komprimieren. Jeder Codec besteht aus zwei Objekten, einem Encoder und einem Decoder. In diesem Teil der Dokumentation wird beschrieben, wie die Funktionen des Windows Media Audio und der Video Codecs verwendet werden, um komprimierte Datenströme zu erzeugen und zu nutzen.

> [!Note]  
> Diese Dokumentation richtet sich hauptsächlich an Entwickler, die Windows Media-Codecs in Ihren C++-basierten Medienanwendungen verwenden möchten. Eine technische Übersicht über die Features der Windows Media-Codecs finden Sie unter [Informationen zu Windows Media Codecs](about-the-windows-media-codecs.md).

 

Der Begriff " *Codec* " ist eine Zusammenstellung der Begriffe "Kompressor" und "Debug". Ein Codec wird normalerweise als Paar von COM-Objekten implementiert: einer für Codierungs Inhalte und ein anderer zum Decodieren von Inhalt. In einigen Fällen belegen die COM-Objekte dieselbe dynamisch verknüpfte Bibliothek (dll).

Jedes Codec-Objekt implementiert zwei separate, aber ähnliche Schnittstellen:



| Schnittstelle                              | BESCHREIBUNG                                 |
|----------------------------------------|---------------------------------------------|
| [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Kompatibel mit Microsoft Media Foundation. |
| [**Imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Kompatibel mit DirectShow.                 |



 

Es gibt nicht nur verschiedene Codecs für Audiodaten und Videos, sondern auch verschiedene Codecs für verschiedene Arten von Inhalten, die Sie möglicherweise in eine Audiodatei oder Videodatei einfügen möchten. Die Algorithmen, die zum Komprimieren und decoden von Daten für gesprochene Wörter verwendet werden, unterscheiden sich von den Algorithmen zum Komprimieren und decoden von Musikdaten.

## <a name="codec-descriptions"></a>Codec-Beschreibungen

In der folgenden Tabelle werden die vorgesehenen Verwendungen der Windows Media Codecs beschrieben.



| Codec                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Media Audio](windowsmediaaudioencoder.md)                       | Ein Audiocodec, der drei Kategorien von codiertem Inhalt unterstützt: Standard, Professional und Lossless.                                                                                                                                                                                      |
| [Windows Media Audio Stimme](windowsmediaaudiovoiceencoder.md)            | Audiocodec, der für die Codierung der menschlichen Stimme bei hohen Komprimierungs Verhältnissen optimiert ist. Dies ist der bevorzugte Codec für Streams, die größtenteils aus gesprochenen Wörtern bestehen. Für Inhalte, die gemischt Musik und Sprache sind, kann dieser Codec den verwendeten Codierungs Algorithmus dynamisch ändern, um eine optimale Qualität zu erzielen. |
| [Windows Media Video 9](windowsmediavideo9encoder.md)                    | Ein Videocodec, der vier Kategorien von codiertem Inhalt unterstützt: einfaches Profil, Hauptprofil, erweitertes Profil und Image.                                                                                                                                                                  |
| [Windows Media Video 9-Bildschirm](usingthewindowsmediavideo9screencodec.md) | Videocodec, der für die Codierung sequenzieller Screenshots von Computermonitoren optimiert ist. Dieser Codec wird häufig für Software Schulungen oder-Unterstützung verwendet, indem Überwachungs Images aufgezeichnet werden, während Computeranwendungen verwendet werden.                                                                         |



 

Die neuesten Versionen der Codec-Objekte ermöglichen auch den Zugriff auf einige Legacy-Codecs, einschließlich Windows Media Video 7 und 8, Windows Media Screen 7, ältere Microsoft MPEG-4-Codecs und Microsoft ISO MPEG-4-Codecs.

> [!Note]  
> In dieser Dokumentation werden diese veralteten Codecs nicht behandelt. Es werden nur die aktuellen Versionen von Codecs behandelt.

 

Verwenden Sie für ältere Codecs dieselben Prozeduren wie bei der Verwendung der aktuellen Codecs. Beachten Sie jedoch, dass nicht alle Funktionen in allen Codecs unterstützt werden.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Informationen zu Windows Media-Codecs](about-the-windows-media-codecs.md)
-   [Verwenden der Codec-und DSP-Objekte](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [Codierungs Methoden](encodingmethods.md)
-   [Codec-Implementierung](codecimplementation.md)
-   [Das Leaky Bucket-Puffer Modell](the-leaky-bucket-buffer-model.md)
-   [Arbeiten mit Codec-DMOS](workingwithcodecdmos.md)
-   [Arbeiten mit Codec-MFTs](workingwithcodecmfts.md)
-   [Arbeiten mit Audiodaten](workingwithaudio.md)
-   [Arbeiten mit Videos](workingwithvideo.md)
-   [Speichern von komprimierten Medien in AVI-Dateien](storingcompressedmediainavifiles.md)
-   [Verwenden der VBR-Codierung](usingvbrencoding.md)
-   [Verwenden von Two-Pass Codierung](usingtwoencodingpasses.md)
-   [Codierungs Statistiken werden erhalten](gettingencodingstatistics.md)
-   [Verwenden von Dateneinheiten Erweiterungen](usingdataunitextensions.md)
-   [Codec-und DSP-IPropertyBag-Konstanten](codecanddspproperties.md)
-   [Inhaltsverzeichnis (Inhaltsverzeichnis)](toc-parser.md)
-   [FAQ zu Windows Media Codec](frequentlyaskedquestions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md)
</dt> <dt>

[Medientechnologien für Windows](/previous-versions/bg125389(v=msdn.10))
</dt> </dl>

 

 
