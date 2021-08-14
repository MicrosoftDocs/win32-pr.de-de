---
description: Legt die Toleranz in Millisekunden fest, die verwendet wird, wenn die ASF-Medienquelle iterative Suchungen ausführt.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8cfc1ef656e1cff3da4bb33f19a3c2176729035f94a194a4ede21354f5dbc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874131"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Tolerance In \_ \_ MilliSecond -Eigenschaft

Legt die Toleranz in Millisekunden fest, die verwendet wird, wenn die ASF-Medienquelle iterative Suchungen ausführt.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Hinweise

Verwenden Sie diese Eigenschaft, um die ASF-Medienquelle zu konfigurieren. Übergeben Sie zum Festlegen der -Eigenschaft einen **IPropertyStore-Zeiger** an den Quellre resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

Diese Eigenschaft gilt nur, wenn die iterative Suche aktiviert ist. Weitere Informationen finden Sie unter [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

Der iterative Suchalgorithmus hält an, wenn er ein Paket findet, dessen Abstand zur Suchzeit innerhalb der angegebenen Toleranz liegt. Der Standardwert ist 8.000 Millisekunden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server 2008 \[ \| R2-Desktop-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




