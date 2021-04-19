---
description: Der Windows Media MP3-Decoder decodiert Audiodateien, die in den folgenden Formaten codiert wurden.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Windows Media MP3-Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366877"
---
# <a name="windows-media-mp3-decoder"></a>Windows Media MP3-Decoder

Der Windows Media MP3-Decoder decodiert Audiodateien, die in den folgenden Formaten codiert wurden.

-   ISO/IEC 11172-3 (MPEG-1-Audiodatei) Ebene 3
-   ISO/IEC 13818-3 (MPEG-2-Audiodatei) Layer 3, niedrige Stichproben Häufigkeits Erweiterung

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) für den Windows Media MP3-Decoder wird durch die Konstante **CLSID \_ CMP3DecMediaObject** dargestellt. Sie können eine Instanz des MP3-Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="interfaces"></a>Schnittstellen

Ein MP3-Decoder-Objekt macht die **imediaobject** -Schnittstelle verfügbar, sodass das Objekt als DirectX Media Object (DMO) verwendet werden kann, und stellt die **imftransform** -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.

Ein Windows Media MP3-Decoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird. In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Windows Media MP3-Decoder als DMO oder MFT verhält.



| Betriebssystem | Decoderverhalten                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP       | Ein Windows Media MP3-Decoder verhält sich immer als DMO.                                                                                                                                           |
| Windows Vista    | Standardmäßig verhält sich ein Windows Media MP3-Decoder als DMO. Wenn Sie eine **imftransform** -Schnittstelle oder eine **IPropertyStore** -Schnittstelle auf einem Windows Media MP3-Decoder abrufen, verhält sie sich als MFT. |
| Windows 7        | Standardmäßig verhält sich ein Windows Media MP3-Decoder als DMO. Wenn Sie eine **imftransform** -Schnittstelle für einen Windows Media MP3-Decoder erhalten, verhält sie sich wie eine MFT.                                    |



 

## <a name="input-formats"></a>Eingabeformate

In der folgenden Tabelle wird das audioformattag angezeigt, das den vom Windows Media MP3-Decoder unterstützten Eingabetyp darstellt.



| Tagkonstante formatieren      | Tagwert formatieren | Audioformat     |
|--------------------------|------------------|------------------|
| Wave- \_ Format \_ MPEGLAYER3 | 0x55             | ISO MPEG Layer 3 |



 

## <a name="output-formats"></a>Ausgabeformate

Die folgende Tabelle zeigt die audioformattags, die die vom Windows Media MP3-Decoder unterstützten Ausgabetypen darstellen.



| Tagkonstante formatieren       | Tagwert formatieren | Audioformat                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| PCM im Wave- \_ Format \_         | 0x0001           | PCM-Format (bei Verwendung als DMO oder MFT)                                   |
| "Wave \_ Format \_ IEEE \_ float" | 0x0003           | IEEE-Gleit Komma (bei Verwendung als MFT)                                   |
| \_erweiterbares Wave-Format \_  | 0xFFFE           | PCM/IEEE-Format in der **WAVEFORMATEXTENSIBLE** -Struktur (bei Verwendung als MFT) |



 

Der Windows Media MP3-Decoder unterstützt und listet die folgenden Ausgabemedien Typen auf.

-   Ein Ausgabetyp, der dieselbe Samplingrate und Anzahl von Kanälen wie der Eingabetyp aufweist.
-   Mono-Ausgabe für Stereo Eingaben.
-   Ausgabetypen mit Bits-Tiefe von 8 und 16.
-   Gleit Komma Ausgabe, wenn der Decoder sich als MFT verhält.

Der Windows Media MP3-Decoder unterstützt die folgenden Ausgabemedien Typen, aber listet sie nicht auf.

-   Ein Ausgabetyp mit der Hälfte der Samplingrate für den Eingabetyp.
-   Ein Ausgabetyp, der eine vierte Samplingrate für den Eingabetyp aufweist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Mp3dmod.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codec-Implementierung](codecimplementation.md)
</dt> </dl>

 

 




