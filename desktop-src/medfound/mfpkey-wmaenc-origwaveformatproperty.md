---
description: Gibt die WAVEFORMATEX-Struktur an, die den Audioinhalt der Eingabe beschreibt.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: MFPKEY_WMAENC_ORIGWAVEFORMAT-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df477daa61e39eb6b2a86aa26c27de4088e943d41f40ac9b708a0201698088c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113140"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a>MFPKEY \_ WMAENC \_ ORIGWAVEFORMAT-Eigenschaft

Gibt die [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) an, die den Audioinhalt der Eingabe beschreibt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMACOriginalWaveFormat

## <a name="data-type"></a>Datentyp

VT \_ ARRAY \| VT \_ UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) als Bytearray)

## <a name="remarks"></a>Hinweise

Beim Transcodieren Windows Medienaudio-basierten Inhalten in eine niedrigere Bitrate können Sie die [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) des Inhalts an den Codec übergeben, damit der Codec seine Algorithmen optimieren kann. Dieses Feature, das als intelligente Rekomprimierung bezeichnet wird, bietet bessere Ergebnisse als das Dekomprimieren des Inhalts und das anschließende Einsenden der rekonstruierten PCM-Beispiele über den Codec.

Wenn Sie die [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) übergeben, schließen Sie alle zusätzlichen Bytes am Ende der durch **WAVEFORMATEX.cbSize angegebenen Struktur ein.**

Der Audioencoder akzeptiert nur Ein- und Ausgaben, für die die Anzahl der Kanäle, Bits pro Stichprobe und Abtastrate identisch sind. Sie können Inhalte nur in eine niedrigere Bitrate innerhalb dieser Parameter transcodieren. In jedem Fall müssen Sie den Inhalt decodieren und die unkomprimierten Beispiele als Eingabe an den Encoder übergeben. Durch Festlegen dieser Eigenschaft erhält der Encoder einige Informationen zur Verarbeitung, die bereits für den Inhalt ausgeführt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
