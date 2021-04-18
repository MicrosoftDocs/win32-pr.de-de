---
description: Legt die Toleranz (in Millisekunden) fest, die verwendet wird, wenn die ASF-Medienquelle iterative Suchvorgänge ausführt.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106351846"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a>Mfpkey \_ asfmediasource \_ iterativeseek \_ Tolerance \_ in \_ millisecond (Eigenschaft)

Legt die Toleranz (in Millisekunden) fest, die verwendet wird, wenn die ASF-Medienquelle iterative Suchvorgänge ausführt.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Eigenschaft, um die ASF-Medienquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Diese Eigenschaft gilt nur, wenn iteratives suchen aktiviert ist. Weitere Informationen finden Sie unter [mfpkey \_ asfmediasource \_ iterativeseekifnoindex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

Der iterative Suchalgorithmus stoppt, wenn er ein Paket findet, dessen Abstand von der Suchzeit innerhalb der angegebenen Toleranz liegt. Der Standardwert ist 8000 Millisekunden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




