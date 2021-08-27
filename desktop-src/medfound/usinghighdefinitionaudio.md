---
description: Verwenden High-Definition Audio
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Verwenden High-Definition Audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3eac918929b6495401a0eeaee31fe6d7a01d2df0eced9866da829381392edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737333"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a>Verwenden High-Definition Audio (Microsoft Media Foundation)

High-Definition-Audio im Kontext der Windows Media Audio-Codecs ist ein beliebiger Audiotyp mit mehr als zwei Kanälen oder mehr als 16 Bits pro Beispiel. High-Definition-Audio wird von den kategorien Professional und Lossless des Windows [Media Audio Encoder unterstützt.](windowsmediaaudioencoder.md)

Unkomprimierte High-Definition-Audiotypen werden mithilfe der [**WAVEFORMATEXTENSIBLE-Struktur**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) definiert. **WAVEFORMATEXTENSIBLE** ist eine strukturierte Erweiterung der [**WAVEFORMATEX-Struktur.**](/previous-versions/dd757713(v=vs.85)) Wenn Sie DMOs verwenden, muss der **formattype-Member** der [**DMO MEDIA \_ \_ TYPE-Struktur,**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) die einen high-definition-Audiotyp beschreibt, auf WMCFORMAT WaveFormatEx festgelegt werden, genau wie für normale Audiodaten. Es gibt keinen speziellen Formatbezeichner für \_ **WAVEFORMATEXTENSIBLE**. Wenn ein Format **WAVEFORMATEXTENSIBLE verwendet,** müssen Sie das **cbSize-Member** der **WAVEFORMATEX-Struktur** auf 22 festlegen.

Wenn Sie Media Foundation, können Sie den richtigen Medientyp aus einer [**WAVEFORMATEXTENSIBLE-Struktur**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) erstellen, indem Sie die [**MFInitMediaTypeFromWaveFormatEx-Funktion verwenden.**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex)

Die vom Windows Media Audio 10 Professional-Codec unterstützten Ausgabetypen mit mehreren Kanälen verwenden [**nicht WAVEFORMATEXTENSIBLE,**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))sondern melden die richtige Anzahl von Kanälen und Bits pro Beispiel in der [**WAVEFORMATEX-Struktur.**](/previous-versions/dd757713(v=vs.85)) Wie bei allen Audiotypen, die komprimierte Windows Medienaudioinhalte beschreiben, werden zusätzliche Informationen an die **WAVEFORMATEX-Struktur** angefügt, die vom Decoder für die Dekomprimierung verwendet wird.

## <a name="decoding-high-definition-audio"></a>Decodieren High-Definition Audio

Um High-Definition-Audio zu decodieren, müssen Sie die [ \_ MFPKEY W \_ DEFINITIONSC HIRESOUTPUT-Eigenschaft](mfpkey-wmadec-hiresoutputproperty.md) auf VARIANT \_ TRUE festlegen. Wenn diese Eigenschaft nicht festgelegt ist, liefert der Decoder Stereoinhalte mit maximal 16 Bits pro Stichprobe, unabhängig vom komprimierten Format.

> [!Note]  
> High-Definition-Audio wird nur für Windows XP, Windows Vista und höher unterstützt. In früheren Versionen von Windows werden Windows mit hoher Definition codierte Medienaudioinhalte als Zweikanalaudio mit maximal 16 Bits pro Beispiel gerendert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Audio](workingwithaudio.md)
</dt> </dl>

 

 
