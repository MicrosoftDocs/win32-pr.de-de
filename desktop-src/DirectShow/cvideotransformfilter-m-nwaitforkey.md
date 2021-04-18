---
description: Die aktuelle maximale Anzahl der zu löschenden Delta Frames.
ms.assetid: d14c594e-55ab-42c2-bdb0-6829f71d02dd
title: 'Cvideotransformfilter:: m_nWaitForKey Member (vtrans. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_nWaitForKey
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a168a26816825c33c0e047d93cc8b14ebd0f3536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365177"
---
# <a name="cvideotransformfilterm_nwaitforkey-member"></a>Cvideotransformfilter:: m \_ nwaitforkey-Member

Die aktuelle maximale Anzahl der zu löschenden Delta Frames. Obwohl diese Variable größer als 0 (null) ist, löscht der Filter Frames, bis ein Keyframe erreicht wird. Für jeden abgelegten Rahmen verringert der Filter diese Variable um eins, wodurch verhindert wird, dass der Filter eine übermäßige Anzahl von Frames löscht. Nach 30 Delta Frames in einer Zeile ohne Keyframes beginnt der Filter erneut mit der Übermittlung von Frames.

## <a name="syntax"></a>Syntax


```C++
int m_nWaitForKey;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cvideotransformfilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




