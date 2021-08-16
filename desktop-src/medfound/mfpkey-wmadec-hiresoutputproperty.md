---
description: Gibt an, ob der Audiodecoder eine Ausgabe mit hoher Auflösung bereitstellen soll.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: MFPKEY_WMADEC_HIRESOUTPUT-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe5226babc8fd40875ec11cfa0b03345ba0b9c1a914b45b5ad79284f79d92130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872538"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a>MFPKEY \_ WUMAC \_ HIRESOUTPUT-Eigenschaft

Gibt an, ob der Audiodecoder eine Ausgabe mit hoher Auflösung bereitstellen soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMACHiResOutput

## <a name="data-type"></a>Datentyp

**VT \_ BOOL**

## <a name="default-value"></a>Standardwert

**VARIANT \_ FALSE**

## <a name="remarks"></a>Hinweise

Legen Sie diese Eigenschaft auf VARIANT \_ TRUE fest, um Multichannel- oder 24-Bit-Audioinhalte oder Audiodaten mit einer Abtastrate von mehr als 48.000 Hz zu decodieren. Wenn der Inhalt in hoher Auflösung codiert ist, diese Eigenschaft jedoch VARIANT \_ FALSE ist, gelten die folgenden Verhaltensweisen:

-   Die DMO Ausgabe ist auf Stereo mit 16 Bit und 48 KHz beschränkt.
-   Der MFT zählt Ausgabemodi auf, die auf 16 Bit beschränkt sind und keine Änderungen an der Kanalanzahl oder Samplingrate beinhalten.

Die Eigenschaften von Audio mit hoher Auflösung werden in einer [**WAVEFORMATEXTENSIBLE-Struktur**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) übergeben, nicht [**in WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85))

Eine Ausgabe mit hoher Auflösung ist nur verfügbar, wenn der Decoder auf Windows XP oder höher ausgeführt wird. Sie können diese Eigenschaft unabhängig vom Betriebssystem festlegen, unter dem Ihre Anwendung ausgeführt wird. Bei Versionen von Windows vor Windows XP ignoriert der Decoder diese Einstellung und liefert eine Standardausgabe.

Viele Player (einschließlich Windows Media Player 9er Serie und höher) legen diesen Wert für alle Inhalte fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
