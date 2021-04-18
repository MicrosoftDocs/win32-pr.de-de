---
description: Gibt an, ob der Audiodecoder eine hochauflösende Ausgabe bereitstellt.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: MFPKEY_WMADEC_HIRESOUTPUT-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345268"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a>Mfpkey \_ wmadec \_ hiresoutput (Eigenschaft)

Gibt an, ob der Audiodecoder eine hochauflösende Ausgabe bereitstellt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmachiresoutput

## <a name="data-type"></a>Datentyp

**VT \_ bool**

## <a name="default-value"></a>Standardwert

**Variant \_ false**

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft auf Variant true fest, \_ um Multichannel-oder 24-Bit-Audioinhalte zu decodieren, oder Audiodaten mit einer Stichprobenrate größer als 48.000 Hz. Wenn der Inhalt in hoher Auflösung codiert ist, diese Eigenschaft aber Variant \_ false ist, gelten die folgenden Verhaltensweisen:

-   Die DMO-Ausgabe wird auf einen 16-Bit-, 48-kHz-Stereo Wert beschränkt.
-   Der MFT listet Ausgabe Modi auf, die auf 16 Bits beschränkt sind und keine Änderungen in der Kanalanzahl oder der Samplingrate beinhalten.

Die Eigenschaften von hochauflösende Audiodaten werden in einer [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) -Struktur, nicht in [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)), weitergegeben.

Die Ausgabe mit hoher Auflösung ist nur verfügbar, wenn der Decoder unter Windows XP oder höher ausgeführt wird. Sie können diese Eigenschaft unabhängig von dem Betriebssystem festlegen, auf dem Ihre Anwendung ausgeführt wird. Unter Windows-Versionen vor Windows XP ignoriert der Decoder diese Einstellung und stellt eine Standardausgabe bereit.

Viele Spieler (einschließlich Windows Media Player 9-Serie und höher) legen diesen Wert für den gesamten Inhalt fest.

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

 

 
