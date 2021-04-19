---
description: Ein Encoder konvertiert unkomprimierte Audiodaten oder Videos in komprimierte Pakete in dem Format, das von der Anwendung angegeben wird. Zum Umrechnen von Mediendateien in das ASF-Format können Sie Windows Media-und Video Codecs verwenden.
ms.assetid: 6dcf12d0-ea37-446b-a807-2b27fd1f6124
title: Windows Media Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a642702562cbb6a70b0380deb196c70c4f8207b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354269"
---
# <a name="windows-media-encoders"></a>Windows Media Encoder

Ein Encoder konvertiert unkomprimierte Audiodaten oder Videos in komprimierte Pakete in dem Format, das von der Anwendung angegeben wird. Zum Umrechnen von Mediendateien in das ASF-Format können Sie Windows Media-und Video Codecs verwenden.

Ein Encoder wird durch die GUID identifiziert, die die Kategorie darstellt: Audiodaten oder Video. Der Ausgabetyp des Encoders wird durch die Haupt-und Untertyp-GUID eines Medientyps dargestellt.

-   Windows Media-Audiocodecs

    Kategorie: **\_ \_ \_ Audioencoder der MFT-Kategorie**

    Haupttyp: MF MediaType \_ -Audiodatei

    SubType: MF Audioformat \_ WMAudioV9, MF Audioformat \_ WMAudioV8, MF Audioformat \_ wmaudio \_ Lossless, MF Audioformat \_ wmaspdif

-   Windows Media-Video Codecs

    Kategorie: **\_ \_ Video \_ Encoder der MFT-Kategorie**

    Haupttyp: MF MediaType- \_ Video

    Untertyp: MF-Format \_ WVC1, MF-Format \_ WMV3, MF-Format \_ WMV2, MF-Format \_ WMV1

Diese Encoder werden als [Media Foundation Transform](media-foundation-transforms.md) (MFT) implementiert, und Media Foundation ermöglicht den Zugriff auf die Anwendung über die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle des Encoder. Wenn Sie Pipeline Schicht Komponenten für die ASF-Codierung verwenden, wird der Encoder-MFT als Transformations Knoten in die Pipeline eingefügt, da er für das Transformieren von Mediendaten verantwortlich ist, die durch die Quelle in die Senke fließen. Wenn die Quelle ein komprimierter Typ ist, fügt die Pipeline die erforderlichen decoderer hinzu, um die Quelle in einen unkomprimierten Typ zu konvertieren. Ein Encoder verfügt über einen Eingabestream und einen Ausgabestream. Der Encoder empfängt Eingabedaten und erzeugt codierte Daten entsprechend der Konfiguration und dem Format, die von der Anwendung vor der Codierungs Sitzung festgelegt wurden. Das Format des Ausgabestreams wird durch einen Medientyp beschrieben.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                                              | BESCHREIBUNG                                                                                 |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Instanziieren eines MFT-Encoders](instantiating-the-encoder-mft.md)                  | Erläutert, wie der Encoder erstellt wird.                                                         |
| [Codierungs Eigenschaften](configuring-the-encoder.md)                                 | Erläutert das Konfigurieren des Encoders durch Festlegen entsprechender Eigenschaften für den Encoder-MFT. |
| [Medientyp Aushandlung für den Encoder](media-type-negotiation-on-the-encoder.md) | Erläutert, wie Eingabe-und Ausgabemedien Typen für den Encoder festgelegt werden.                            |
| [Konfigurieren eines WMV-Encoders](configuring-a-wmv-encoder.md)                         | Erläutert das Konfigurieren eines Windows Media Video-Encoders (WMV).                              |
| [Festlegen eines Ausgabe Typs für einen WMA-Encoder](configuring-a-wma-encoder.md)          | Erläutert, wie ein Ausgabetyp für einen Windows Media Audio (WMA)-Encoder festgelegt wird.                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponenten der Pipeline Schicht-ASF](pipeline-layer-asf-components.md)
</dt> </dl>

 

 



