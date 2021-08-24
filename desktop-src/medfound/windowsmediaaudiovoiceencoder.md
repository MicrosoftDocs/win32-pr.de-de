---
description: Der Windows Media Audio Voice-Encoder ist für die Codierung der menschlichen Stimme mit hohen Komprimierungsverhältnisse optimiert. Dies ist der bevorzugte Encoder für Streams, die größtenteils aus gesprochenen Wörtern bestehen.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Windows Media Audio Voice Encoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c107e4e09309ff0ed56e899d3ec2cd0c9d372261b48231b4530ed3222ee3a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462426"
---
# <a name="windows-media-audio-voice-encoder"></a>Windows Media Audio Voice Encoder

Der Windows Media Audio Voice-Encoder ist für die Codierung der menschlichen Stimme mit hohen Komprimierungsverhältnisse optimiert. Dies ist der bevorzugte Encoder für Streams, die größtenteils aus gesprochenen Wörtern bestehen.

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) für den Windows Media Audio Voice-Encoder wird durch die Konstante **CLSID \_ CWMSPEncMediaObject2 dargestellt.** Sie können eine Instanz des Voiceencoder erstellen, indem Sie **CoCreateInstance aufrufen.**

## <a name="output-formats"></a>Ausgabeformate

Windows Media Audio Voice-codierter Inhalt wird durch das Formattag 0x00A.

## <a name="encoder-properties"></a>Encodereigenschaften

Der Windows Media Audio Voice-Encoder unterstützt die folgenden Eigenschaften.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></td>
<td>Gibt das Pufferfenster in Millisekunden an, das für den Sprachcodec verwendet wird.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></td>
<td>Gibt die Encoderlatenz in Paketeinheiten an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></td>
<td>Gibt die Teile des Inhalts an, die vom Sprachcodec als Musik codiert werden sollen.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></td>
<td>Gibt den Modus des Sprachcodecs an.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmoe.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Verwenden des Windows Media Audio Voice Codec](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




