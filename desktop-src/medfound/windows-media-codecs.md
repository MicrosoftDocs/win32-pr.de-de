---
description: Die Windows Medienaudio- und Videocodecs sind eine Sammlung von Objekten, mit denen Sie digitale Mediendaten komprimieren und dekomprimieren können.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Windows Media-Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 863bb21e17200016317ce273ecb8e2493b9d6bea7d19f92f3f397fb61b88eba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972529"
---
# <a name="windows-media-codecs"></a>Windows Media-Codecs

Die Windows Medienaudio- und Videocodecs sind eine Sammlung von Objekten, mit denen Sie digitale Mediendaten komprimieren und dekomprimieren können. Jeder Codec besteht aus zwei Objekten, einem Encoder und einem Decoder. In diesem Teil der Dokumentation wird beschrieben, wie Sie die Features der Windows-Codecs für Medienaudio und -video verwenden, um komprimierte Datenströme zu erzeugen und zu nutzen.

> [!Note]  
> Diese Dokumentation richtet sich in erster Linie an Entwickler, die Windows Mediencodecs in ihren C++-basierten Medienanwendungen verwenden möchten. Eine technische Übersicht über die Features der Windows Mediencodecs finden Sie unter Informationen zu Windows [Mediencodecs.](about-the-windows-media-codecs.md)

 

Der Begriff *Codec* ist eine Auskommentierung der Begriffe "Primieren" und "Dekomprimieren". Ein Codec wird in der Regel als Paar von COM-Objekten implementiert: eines zum Codieren von Inhalten und ein weiteres zum Decodieren von Inhalt. In einigen Fällen belegen die COM-Objekte dieselbe dynamisch verknüpfte Bibliothek (DLL).

Jedes Codecobjekt implementiert zwei separate, aber ähnliche Schnittstellen:



| Schnittstelle                              | BESCHREIBUNG                                 |
|----------------------------------------|---------------------------------------------|
| [**VORRÜBERSETZUNGTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Kompatibel mit Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Kompatibel mit DirectShow.                 |



 

Es gibt nicht nur verschiedene Codecs für Audio und Video, sondern auch unterschiedliche Codecs für verschiedene Arten von Inhalten, die Sie in eine Audio- oder Videodatei speichern möchten. Die Algorithmen zum Komprimieren und Dekomprimieren von Daten für gesprochene Wörter unterscheiden sich von den Algorithmen zum Komprimieren und Dekomprimieren von Musikdaten.

## <a name="codec-descriptions"></a>Codecbeschreibungen

In der folgenden Tabelle werden die vorgesehenen Verwendungsmöglichkeiten der Windows Mediencodecs beschrieben.



| Codec                                                                     | Beschreibung                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Media Audio](windowsmediaaudioencoder.md)                       | Ein Audiocodec, der drei Kategorien von codiertem Inhalt unterstützt: Standard, Professional und Verlustlos.                                                                                                                                                                                      |
| [Windows Media Audio Voice](windowsmediaaudiovoiceencoder.md)            | Audiocodec, der für die Codierung der menschlichen Stimme mit hohen Komprimierungsverhältnisse optimiert ist. Dies ist der bevorzugte Codec für Streams, die größtenteils aus gesprochenen Wörtern bestehen. Bei Inhalten, bei denen es sich um gemischte Musik und Sprache handelt, kann dieser Codec den verwendeten Codierungsalgorithmus dynamisch ändern, um eine optimale Qualität zu erhalten. |
| [Windows Media Video 9](windowsmediavideo9encoder.md)                    | Ein Videocodec, der vier Kategorien codierter Inhalte unterstützt: Einfaches Profil, Hauptprofil, Erweitertes Profil und Bild.                                                                                                                                                                  |
| [Windows Media Video 9 Screen](usingthewindowsmediavideo9screencodec.md) | Videocodec, der für die Codierung sequenzieller Screenshots von Computermonitoren optimiert ist. Dieser Codec wird häufig für Softwaretraining oder -unterstützung verwendet, indem Monitorbilder während der Verwendung von Computeranwendungen aufzeichnen.                                                                         |



 

Die neuesten Versionen der Codecobjekte ermöglichen auch den Zugriff auf einige ältere Codecs, einschließlich Windows Media Video 7 und 8, Windows Media Screen 7, der älteren Microsoft MPEG-4-Codecs und der Microsoft ISO MPEG-4-Codecs.

> [!Note]  
> Diese Legacycodecs werden in dieser Dokumentation nicht beschrieben. Es werden nur die aktuellen Versionen von Codecs behandelt.

 

Verwenden Sie für ältere Codecs die gleichen Verfahren wie bei der Verwendung der aktuellen Codecs. Denken Sie jedoch daran, dass nicht alle Features in allen Codecs unterstützt werden.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Informationen zu Windows Mediencodecs](about-the-windows-media-codecs.md)
-   [Verwenden der Codec- und DSP-Objekte](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [Codierungsmethoden](encodingmethods.md)
-   [Codecimplementierung](codecimplementation.md)
-   [Das Leaky Bucket Buffer-Modell](the-leaky-bucket-buffer-model.md)
-   [Arbeiten mit Codec-DMOs](workingwithcodecdmos.md)
-   [Arbeiten mit Codec-MFTs](workingwithcodecmfts.md)
-   [Arbeiten mit Audio](workingwithaudio.md)
-   [Arbeiten mit Videos](workingwithvideo.md)
-   [Speichern komprimierter Medien in AVI-Dateien](storingcompressedmediainavifiles.md)
-   [Verwenden der VBR-Codierung](usingvbrencoding.md)
-   [Verwenden Two-Pass Codierung](usingtwoencodingpasses.md)
-   [Abrufen von Codierungsstatistiken](gettingencodingstatistics.md)
-   [Verwenden von Dateneinheitserweiterungen](usingdataunitextensions.md)
-   [Codec- und DSP-IPropertyBag-Konstanten](codecanddspproperties.md)
-   [Inhaltsverzeichnisparser](toc-parser.md)
-   [Windows Häufig gestellte Fragen zum Mediencodec](frequentlyaskedquestions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmierhandbuch](media-foundation-programming-guide.md)
</dt> <dt>

[Medientechnologien für Windows](/previous-versions/bg125389(v=msdn.10))
</dt> </dl>

 

 
