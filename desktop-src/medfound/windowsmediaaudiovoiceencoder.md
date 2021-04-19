---
description: Der Windows Media Audio Voice-Encoder ist für die Codierung der menschlichen Stimme bei hohen Komprimierungs Verhältnissen optimiert. Dies ist der bevorzugte Encoder für Streams, die größtenteils aus gesprochenen Wörtern bestehen.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Windows Media Audio sprach Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370789"
---
# <a name="windows-media-audio-voice-encoder"></a>Windows Media Audio sprach Encoder

Der Windows Media Audio Voice-Encoder ist für die Codierung der menschlichen Stimme bei hohen Komprimierungs Verhältnissen optimiert. Dies ist der bevorzugte Encoder für Streams, die größtenteils aus gesprochenen Wörtern bestehen.

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) für den Windows Media Audio Voice-Encoder wird durch die Konstante **CLSID \_ CWMSPEncMediaObject2** dargestellt. Sie können eine Instanz des Voice-Encoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="output-formats"></a>Ausgabeformate

Windows Media Audio sprach codierter Inhalt wird durch das Format-Tag 0x00a identifiziert.

## <a name="encoder-properties"></a>Codierungs Eigenschaften

Der Windows Media Audio Voice-Encoder unterstützt die folgenden Eigenschaften.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></td>
<td>Gibt das für den voicecodec verwendete Puffer Fenster in Millisekunden an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></td>
<td>Gibt die encoderwartezeit in Paketeinheiten an.<br/> <dl> Windows XP und höher.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></td>
<td>Gibt die Inhalts Teile an, die vom Voice-Codec als Musik codiert werden sollen.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></td>
<td>Gibt den Modus des voicecodec an.<br/> <dl> Windows XP und höher.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmoe.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Verwenden des Windows Media Audio Voice-Codecs](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




