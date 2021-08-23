---
description: Medientypaushandlung auf dem Encoder
ms.assetid: c8ae543e-68f7-4c74-9cb7-2a200bd51820
title: Medientypaushandlung auf dem Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ac5dd5a107633feba4ce2a74da7e9aea7e9f71d51be1b5cad5b85ab4adda35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941510"
---
# <a name="media-type-negotiation-on-the-encoder"></a>Medientypaushandlung auf dem Encoder

In Microsoft Media Foundation werden Encoder als [Media Foundation Transformationen](media-foundation-transforms.md) (MFTs) mit einer Eingabe und einer Ausgabe implementiert. Vor einer Codierungssitzung muss ein Encoder die Merkmale des Streams kennen, den er als Eingabe empfängt, und das Format des Streams, den er als Ausgabe erzeugt. Sie müssen die Eingabe- und Ausgabemedientypen und zugehörigen Merkmale festlegen, bevor Sie Daten über den Encoder übergeben. Sie müssen die Eingabe- und Ausgabeformate angeben, indem Sie die entsprechenden [Medientyp-GUIDs](media-type-guids.md) angeben und die Merkmale des Ausgabestreams festlegen, indem Sie die relevanten [Medientypattribute](media-type-attributes.md) für den Ausgabemedientyp festlegen. Ein neu instanziierter Encoder verfügt über keine festgelegten Medientypen.

Der Eingabemedientyp ist ein nicht komprimiertes Format, z. B. PCM-Audio oder RGB-Video. Die vom Encoder verwendeten Formattypen sind auf die von den **VIDEOINFOHEADER-** und **WAVEFORMATEX-Strukturen** beschriebenen Beschränkt. Weitere Informationen zu diesen Strukturen finden Sie in der Windows SDK-Dokumentation. Media Foundation bietet Hilfsfunktionen zum Erstellen von Medientypen aus Formatstrukturen. Beispielsweise initialisiert die [**MFInitMediaTypeFromVideoInfoHeader-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) einen Videotyp aus einer **VIDEOINFOHEADER-Struktur,** und die [**MFInitMediaTypeFromWaveFormatEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) initialisiert einen Videotyp aus einer **WAVEFORMATEX-** oder **WAVEFORMATEXTENSIBLE-Struktur.** Weitere Informationen finden Sie unter [Medientypkonvertierungen.](media-type-conversions.md) Sie müssen den Eingabemedientyp auf dem Encoder festlegen, indem Sie [**DENTRANSFORM::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)aufrufen.

Der Ausgabemedientyp ist das Komprimierungsformat, das im endgültigen Quellstream oder in der endgültigen Quelldatei verwendet wird. Sie können den verfügbaren Ausgabemedientyp erst festlegen, nachdem Sie den Eingabemedientyp festgelegt haben. Sie können die unterstützten Ausgabetypen abrufen, indem [**Sie ÜBERTRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in einer Schleife aufrufen, bis der Encoder **MF E NO MORE \_ \_ \_ \_ TYPES** zurückgibt. Erhöhen Sie den Typindex bei jeder Iteration. Wenn Sie einen geeigneten Medientyp finden, legen Sie den Ausgabemedientyp fest, indem Sie [**ÜBERTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)aufrufen.

Der Entscheidungsfaktor bei der Auswahl des Ausgabemedientyps hängt vom Typ der Codierung und Ihren Codierungsanforderungen ab. Für Audiostreams, die CBR-codiert sind, möchten Sie beispielsweise einen Medientyp suchen, der mit Ihrer Eingabe übereinstimmt und eine Bitrate aufweist, die so nah wie möglich an einem Zielwert liegt.

Wenn Sie einen anderen Codierungsmodus als CBR verwenden möchten, müssen Sie den Modus festlegen und dann die Ausgabetypen für diesen Modus aufzählen, da der Encoder die unterstützten Ausgabetypen je nach Modussatz ändert. Die Eigenschaften, die den Codierungsmodus steuern, sind [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) und [**MFPKEY \_ PASSESUSED.**](mfpkey-passesusedproperty.md) Wenn Sie beispielsweise Ausgabetypen für die VBR-Qualitätscodierung aufzählen, hängt der Medientyp vom Qualitätswert ab, den Sie verwenden möchten. Informationen zum Festlegen dieser Eigenschaften finden Sie unter [Codierungseigenschaften.](configuring-the-encoder.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Instanziieren eines Encoder-MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Medienencoder](windows-media-encoders.md)
</dt> </dl>

 

 



