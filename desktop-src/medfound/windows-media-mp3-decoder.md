---
description: Der Windows Media MP3-Decoder decodiert Audiodateien, die in den folgenden Formaten codiert wurden.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Windows Medien-MP3-Decoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58788a00ddaa43686c3cb4be4a52292edb3fe6c6f81fabbc5b4f3e75c47f0f24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736999"
---
# <a name="windows-media-mp3-decoder"></a>Windows Medien-MP3-Decoder

Der Windows Media MP3-Decoder decodiert Audiodateien, die in den folgenden Formaten codiert wurden.

-   ISO/IEC 11172-3 (MPEG-1 Audio) Layer 3
-   ISO/IEC 13818-3 (MPEG-2 Audio) Layer 3, Erweiterung für niedrige Samplinghäufigkeit

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) für den Windows Media MP3-Decoder wird durch die Konstante **CLSID \_ CMP3DecMediaObject dargestellt.** Sie können eine Instanz des MP3-Decoders erstellen, indem Sie **CoCreateInstance aufrufen.**

## <a name="interfaces"></a>Schnittstellen

Ein MP3-Decoderobjekt macht die **IMediaObject-Schnittstelle** verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und es macht die **METHODETransform-Schnittstelle** verfügbar, sodass das Objekt als Media Foundation Transform (MFT) verwendet werden kann.

Ein Windows Media MP3-Decoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie abrufen und welche Version von Windows wird. Die folgende Tabelle zeigt die Bedingungen, unter denen sich Windows Medien-MP3-Decoder wie ein DMO oder MFT verhält.



| Betriebssystem | Decoderverhalten                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Ein Windows Medien-MP3-Decoder verhält sich immer wie ein DMO.                                                                                                                                           |
| Windows Vista    | Standardmäßig verhält sich ein Windows Media MP3-Decoder wie ein DMO. Wenn Sie eine **BZW.** eine **IPropertyStore-Schnittstelle** für Windows Media MP3-Decoder abrufen, verhält es sich wie ein MFT. |
| Windows 7        | Standardmäßig verhält sich ein Windows Media MP3-Decoder wie ein DMO. Wenn Sie eine **NSVTransform-Schnittstelle** für Windows Media MP3-Decoder abrufen, verhält sie sich wie ein MFT.                                    |



 

## <a name="input-formats"></a>Eingabeformate

Die folgende Tabelle zeigt das Audioformattag, das den eingabetyp darstellt, der vom Windows Media MP3-Decoder unterstützt wird.



| Formattagkonst constant      | Formatieren des Tagwerts | Audioformat     |
|--------------------------|------------------|------------------|
| \_WAVE-FORMAT \_ MPEGLAYER3 | 0x55             | ISO MPEG Layer 3 |



 

## <a name="output-formats"></a>Ausgabeformate

Die folgende Tabelle zeigt die Audioformattags, die die ausgabetypen darstellen, die vom Windows Media MP3-Decoder unterstützt werden.



| Formattagkonst constant       | Formatieren des Tagwerts | Audioformat                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| \_ \_ WAVE-FORMAT PCM         | 0x0001           | PCM-Format (bei Verwendung als DMO oder MFT)                                   |
| WAVE \_ FORMAT \_ IEEE \_ FLOAT | 0x0003           | IEEE-Gleitkomma (bei Verwendung als MFT)                                   |
| ERWEITERBARES \_ \_ WAVE-FORMAT  | 0xFFFE           | PCM/IEEE-Format in **der WAVEFORMATEXTENSIBLE-Struktur** (bei Verwendung als MFT) |



 

Der Windows Media MP3-Decoder unterstützt und aufzählt die folgenden Ausgabemedientypen.

-   Ein Ausgabetyp mit der gleichen Samplingrate und Anzahl von Kanälen wie der Eingabetyp.
-   Mono-Ausgabe für Stereoeingabe.
-   Ausgabetypen mit Bittiefe von 8 und 16.
-   Gleitkommaausgabe, wenn sich der Decoder als MFT verhält.

Der Windows Media MP3-Decoder unterstützt die folgenden Ausgabemedientypen, führt diese aber nicht auf.

-   Ein Ausgabetyp, der die Hälfte der Samplingrate des Eingabetyps auf hat.
-   Ein Ausgabetyp, der ein Viertes der Samplingrate des Eingabetyps hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Mp3dmod.dll</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codecimplementierung](codecimplementation.md)
</dt> </dl>

 

 




