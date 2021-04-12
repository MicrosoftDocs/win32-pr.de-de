---
description: Gibt die WaveFormatEx-Struktur an, die den audioinhaltstyp beschreibt.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: MFPKEY_WMAENC_ORIGWAVEFORMAT-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3475e5578124b8f0a762beddf713f701a5695110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215421"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a>Mfpkey \_ wmaenc \_ origwaveformat (Eigenschaft)

Gibt die [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur an, die den audioinhaltstyp beschreibt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmacoriginalwaveformat

## <a name="data-type"></a>Datentyp

VT \_ array \| VT \_ UI1 ([**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) als Bytearray)

## <a name="remarks"></a>Bemerkungen

Wenn Sie Windows Media Audio basierten Inhalt in eine niedrigere Bitrate transcodieren, können Sie die [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur des Inhalts an den Codec übergeben, damit der Codec seine Algorithmen optimieren kann. Diese Funktion, die als Smart Recompression bezeichnet wird, bietet bessere Ergebnisse als das Dekomprimieren des Inhalts und das anschließende Füttern der rekonstruierten PCM-Beispiele über den Codec.

Schließen Sie beim Übergeben der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur alle zusätzlichen Bytes am Ende der Struktur ein, die von **WaveFormatEx. cbSize** angegeben wird.

Der Audioencoder akzeptiert nur Eingaben und Ausgaben, bei denen die Anzahl der Kanäle, Bits pro Stichprobe und die Stichprobenrate identisch sind. In diesen Parametern können Sie nur Inhalte in eine niedrigere Bitrate transcodieren. In jedem Fall müssen Sie den Inhalt decodieren und die nicht komprimierten Beispiele als Eingabe an den Encoder übergeben. Durch Festlegen dieser Eigenschaft erhält der Encoder einige Informationen über die Verarbeitung, die bereits für den Inhalt durchgeführt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
