---
description: Legt die maximale Anzahl von Such Iterationen fest, die von der ASF-Medienquelle beim Ausführen iterativer Suchvorgänge verwendet werden.
ms.assetid: 5b596faf-1217-424d-ae16-8c9ec6f31af1
title: MFPKEY_ASFMediaSource_IterativeSeek_Max_Count-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfb9268f1def2ab0d489f58cafa0b1720196c7ac
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354279"
---
# <a name="mfpkey_asfmediasource_iterativeseek_max_count-property"></a>Mfpkey \_ asfmediasource \_ iterativeseek \_ Max \_ count (Eigenschaft)

Legt die maximale Anzahl von Such Iterationen fest, die von der ASF-Medienquelle beim Ausführen iterativer Suchvorgänge verwendet werden.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Eigenschaft, um die ASF-Medienquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Diese Eigenschaft gilt nur, wenn iteratives suchen aktiviert ist. Weitere Informationen finden Sie unter [mfpkey \_ asfmediasource \_ iterativeseekifnoindex](mfpkey-asfmediasource-iterativeseekifnoindex.md).

Der gültige Bereich dieser Eigenschaft ist \[ 1-10 ( \] einschließlich). Bei einer höheren Zahl ist das iterative suchen tendenziell genauer, dauert jedoch länger.

Der Standardwert ist 5.

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

 

 




