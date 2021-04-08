---
description: Medientyp Aushandlung für den Encoder
ms.assetid: c8ae543e-68f7-4c74-9cb7-2a200bd51820
title: Medientyp Aushandlung für den Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7845e9d50c5d418198dc0e08313e2e9329ffab8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961210"
---
# <a name="media-type-negotiation-on-the-encoder"></a>Medientyp Aushandlung für den Encoder

In Microsoft Media Foundation werden Encoder als [Media Foundation Transformationen](media-foundation-transforms.md) (MFTs) mit einer Eingabe und einer Ausgabe implementiert. Vor einer Codierungs Sitzung muss ein Encoder die Merkmale des Datenstroms, der als Eingabe empfangen wird, und das Format des Datenstroms, der als Ausgabe erzeugt wird, kennen. Sie müssen die Eingabe-und Ausgabemedien Typen und die zugehörigen Eigenschaften festlegen, bevor Sie Daten über den Encoder übergeben. Sie müssen die Eingabe-und Ausgabeformate angeben, indem Sie die entsprechenden [Medientyp-GUIDs](media-type-guids.md) angeben und die Merkmale des Ausgabestreams festlegen, indem Sie die relevanten [Medientyp Attribute](media-type-attributes.md) für den Ausgabe Medientyp festlegen. Ein neu instanziierte Encoder weist keine festgelegten Medientypen auf.

Der Eingabe Medientyp ist ein unkomprimiertes Format, z. b. PCM-Audiodaten oder RGB-Video. Die vom Encoder verwendeten Format Typen sind auf die Typen beschränkt, die von den **videoinfoheader** -und **WaveFormatEx** -Strukturen beschrieben werden. Weitere Informationen zu diesen Strukturen finden Sie in der Windows SDK-Dokumentation. Media Foundation stellt Hilfsfunktionen zum Erstellen von Medientypen aus Format Strukturen bereit. Beispielsweise initialisiert die Funktion " [**mfinitmediatyetfromvideoinfoheader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) " einen Videotyp aus einer **videoinfoheader** -Struktur, und die Funktion " [**mfinitmediatypeer fromwaveformatex**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) " Initialisiert einen Videotyp aus einer **WaveFormatEx** -oder **WAVEFORMATEXTENSIBLE** -Struktur. Weitere Informationen finden Sie unter [Medientyp Konvertierungen](media-type-conversions.md). Sie müssen den Eingabe Medientyp für den Encoder festlegen, indem Sie [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)aufrufen.

Der Ausgabe Medientyp ist das Komprimierungs Format, das im endgültigen Quelldaten Strom oder in der endgültigen Datei verwendet wird. Sie können den verfügbaren Ausgabe Medientyp erst festlegen, nachdem Sie den Eingabe Medientyp festgelegt haben. Sie können die unterstützten Ausgabetypen abrufen, indem Sie " [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) " in einer Schleife aufrufen, bis der Encoder " **MF \_ E \_ No \_ more \_ types**" zurückgibt. Erhöhen Sie den Typindex bei jeder Iterationen. Wenn Sie einen geeigneten Medientyp finden, legen Sie den Ausgabe Medientyp durch Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)fest.

Der entscheidende Faktor bei der Auswahl des Ausgabemedien Typs hängt vom Codierungstyp und den Codierungs Anforderungen ab. Beispielsweise möchten Sie für Audiodatenströme, die CBR-codiert sind, einen Medientyp suchen, der mit Ihrer Eingabe übereinstimmt, und eine Bitrate haben, die so nah wie möglich an einem Zielwert ist.

Wenn Sie einen anderen Codierungs Modus als CBR verwenden möchten, müssen Sie den-Modus festlegen und dann die Ausgabetypen für diesen Modus auflisten, da der Encoder die unterstützten Ausgabetypen abhängig vom festgelegten Modus ändert. Die Eigenschaften, die den Codierungs Modus steuern, sind [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) und [**mfpkey \_ passesused**](mfpkey-passesusedproperty.md). Wenn Sie z. b. Ausgabetypen für die VBR-Qualitäts Codierung auflisten, hängt der Medientyp von dem Qualitäts Wert ab, den Sie verwenden möchten. Weitere Informationen zum Festlegen dieser Eigenschaften finden Sie unter [Codierungs Eigenschaften](configuring-the-encoder.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Instanziieren eines MFT-Encoders](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 



