---
description: Der Windows Media Audio Voice-Decoder decodiert Datenströme, die vom Windows Media Audio Voice-Encoder codiert wurden.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Windows Media Audio sprach Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369647"
---
# <a name="windows-media-audio-voice-decoder"></a>Windows Media Audio sprach Decoder

Der Windows Media Audio Voice-Decoder decodiert Datenströme, die vom [**Windows Media Audio Voice-Encoder**](windowsmediaaudiovoiceencoder.md)codiert wurden.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) für den Windows Media Audio sprach Decoder wird durch die Konstante **CLSID \_ cwmspdecmediaobject** dargestellt. Sie können eine Instanz des sprach Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="input-formats"></a>Eingabeformate

Windows Media Audio sprach codierter Inhalt wird durch das Format-Tag 0x00a identifiziert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmod.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Verwenden des Windows Media Audio Voice-Codecs](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Windows Media Audio sprach Encoder](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




