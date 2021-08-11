---
description: Ein Encoder konvertiert unkomprimierte Audio- oder Videodaten in komprimierte Pakete in dem von der Anwendung angegebenen Format. Zum Konvertieren von Mediendateien in das ASF-Format können Sie die Windows Medienaudio- und Videocodecs verwenden.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Windows Medienencoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d79ff55e98227c63e9761a8dec5ae068c8b1786c067230548ad0028dbe301a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237289"
---
# <a name="windows-media-encoders"></a>Windows Medienencoder

Ein Encoder konvertiert unkomprimierte Audio- oder Videodaten in komprimierte Pakete in dem von der Anwendung angegebenen Format. Zum Konvertieren von Mediendateien in das ASF-Format können Sie die Windows Medienaudio- und Videocodecs verwenden.

Ein Encoder wird durch die GUID identifiziert, die die Kategorie darstellt: Audio oder Video. Der Ausgabetyp des Encoders wird durch die Haupt- und Untertyp-GUID eines Medientyps dargestellt.

-   Windows Medienaudiocodecs

    Kategorie: **MFT \_ CATEGORY AUDIO \_ \_ ENCODER**

    Haupttyp: MFMediaType \_ Audio

    Untertyp: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Windows Medienvideocodecs

    Kategorie: **MFT \_ CATEGORY VIDEO \_ \_ ENCODER**

    Haupttyp: MFMediaType \_ Video

    Untertyp: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1

Diese Encoder werden als [Media Foundation Transform (MFT)](media-foundation-transforms.md) implementiert, und Media Foundation ermöglicht den Zugriff auf die Anwendung über die [**INTERFACESTransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) des Encoders. Wenn Sie Pipelineebenenkomponenten für die ASF-Codierung verwenden, wird der Encoder-MFT als Transformationsknoten in die Pipeline eingefügt, da er für die Transformation von Mediendaten verantwortlich ist, die durch die Quelle in die Senke fließen. Wenn die Quelle ein komprimierter Typ ist, fügt die Pipeline die erforderlichen Decoder hinzu, um die Quelle in einen nicht komprimierten Typ zu konvertieren. Ein Encoder verfügt über einen Eingabestream und einen Ausgabestream. Der Encoder empfängt Eingabedaten und erzeugt codierte Daten gemäß der Konfiguration und dem Format, die von der Anwendung vor der Codierungssitzung festgelegt wurden. Das Format des Ausgabestreams wird durch einen Medientyp beschrieben.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                                              | BESCHREIBUNG                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Instanziieren eines Encoder-MFT](instantiating-the-encoder-mft.md)                  | Erläutert, wie der Encoder erstellt wird.                                                         |
| [Codierungseigenschaften](configuring-the-encoder.md)                                 | Erläutert, wie der Encoder konfiguriert wird, indem entsprechende Eigenschaften für den Encoder-MFT festgelegt werden. |
| [Medientypaushandlung auf dem Encoder](media-type-negotiation-on-the-encoder.md) | Erläutert, wie Eingabe- und Ausgabemedientypen auf dem Encoder festgelegt werden.                            |
| [Konfigurieren eines WMV-Encoders](configuring-a-wmv-encoder.md)                         | Erläutert, wie sie einen encoder Windows Media Video (WMV) konfigurieren.                              |
| [Festlegen eines Ausgabetyps für einen WMA-Encoder](configuring-a-wma-encoder.md)          | Erläutert, wie ein Ausgabetyp für einen Windows Media Audio-Encoder (WMA) festgelegt wird.                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Komponenten auf Pipelineebene](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



