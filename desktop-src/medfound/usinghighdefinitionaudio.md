---
description: Verwenden High-Definition Audiodaten
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Verwenden High-Definition Audiodaten (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755240"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a>Verwenden High-Definition Audiodaten (Microsoft Media Foundation)

Bei der Verwendung von High-Definition-Audiodaten im Kontext der Windows Media Audio Codecs handelt es sich um einen beliebigen Audiotyp mit mehr als zwei Kanälen oder mehr als 16 Bits pro Stichprobe. High-Definition-Audiodaten werden von den Kategorien "Professional" und "Lossless" des [Windows Media Audio Encoders](windowsmediaaudioencoder.md)unterstützt.

Unkomprimierte High-Definition-Audiotypen werden mithilfe der [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) -Struktur definiert. **WAVEFORMATEXTENSIBLE** ist eine strukturierte Erweiterung der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur. Wenn Sie DMOS verwenden, muss der **Format Type** -Member der [**DMO \_ - \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur, der einen hoch definierbaren Audiotyp beschreibt, auf das wmcformat \_ WaveFormatEx festgelegt werden, so wie es für das normale Audioformat der Fall ist. es gibt keinen speziellen Format Bezeichner für **WAVEFORMATEXTENSIBLE**. Wenn ein Format **WAVEFORMATEXTENSIBLE** verwendet, müssen Sie das **CBSIZE** -Element der **WaveFormatEx** -Struktur auf 22 festlegen.

Wenn Sie Media Foundation verwenden, können Sie den richtigen Medientyp aus einer [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) -Struktur erstellen, indem Sie die [**mfinitmediatypeer fromwaveformatex**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex)-Funktion verwenden.

Die vom Windows Media Audio 10 Professional-Codec unterstützten multikanalausgabetypen verwenden [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))nicht, melden jedoch die richtige Anzahl von Kanälen und Bits pro Stichprobe in der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur. Wie bei allen Audiotypen, die komprimierte Windows Media Audio Inhalt beschreiben, werden zusätzliche Informationen an die **WaveFormatEx** -Struktur angehängt, die vom Decoder für die Dekomprimierung verwendet wird.

## <a name="decoding-high-definition-audio"></a>Decodieren High-Definition Audiodaten

Zum Decodieren von High-Definition-Audiodaten müssen Sie die Eigenschaft [mfpkey \_ wmadec \_ hiresoutput](mfpkey-wmadec-hiresoutputproperty.md) auf Variant \_ true festlegen. Wenn diese Eigenschaft nicht festgelegt ist, stellt der Decoder unabhängig vom komprimierten Format Stereo Inhalte mit maximal 16 Bits pro Beispiel bereit.

> [!Note]  
> High-Definition-Audiodaten werden nur für Windows XP, Windows Vista und höher unterstützt. In früheren Versionen von Windows wird Windows Media Audio mit hoher Definition codierte Inhalt als zwei-Kanal-Audiodaten mit maximal 16 Bits pro Stichprobe gerendert.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Audiodaten](workingwithaudio.md)
</dt> </dl>

 

 
