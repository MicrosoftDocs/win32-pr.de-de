---
description: Legt die maximale Anzahl von Suchiterationen fest, die die ASF-Medienquelle bei iterativen Suchläufen verwendet.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: MFPKEY_ASFMediaSource_IterativeSeek_Max_Count-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183ed13143260f9d6d5de67ba38fcff27ebfd5a6afb01c75a07e92497d571cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874253"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a>MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ Max Count \_ -Eigenschaft

Legt die maximale Anzahl von Suchiterationen fest, die die ASF-Medienquelle bei iterativen Suchläufen verwendet.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Hinweise

Verwenden Sie diese Eigenschaft, um die ASF-Medienquelle zu konfigurieren. Um die Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore-Zeiger** an den Quell resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

Diese Eigenschaft gilt nur, wenn iterative Suche aktiviert ist. Weitere Informationen finden Sie unter [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

Der gültige Bereich dieser Eigenschaft ist \[ einschließlich 1 bis 10. \] Mit einer höheren Zahl ist die iterative Suche in der Regel genauer, dauert aber länger.

Der Standardwert ist 5.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




