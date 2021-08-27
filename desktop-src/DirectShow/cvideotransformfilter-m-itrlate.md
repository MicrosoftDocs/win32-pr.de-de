---
description: Gibt an, wie spät die Beispiele beim Renderer in Referenzzeiteinheiten eintreffen. Syntax.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: CVideoTransformFilter::m_itrLate-Member (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba2d14d19849768538184e54de5ca84b9495371783d57231ab9ad6aa7738718
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075950"
---
# <a name="cvideotransformfilterm_itrlate-member"></a>CVideoTransformFilter::m \_ itrLate-Member

Gibt an, wie spät die Beispiele beim Renderer in Referenzzeiteinheiten eintreffen. Syntax

## <a name="syntax"></a>Syntax


```C++
int m_itrLate;
```



## <a name="remarks"></a>Hinweise

Wenn der Filter eine Qualitätsmeldung von downstream empfängt, speichert er den Lateness-Wert in dieser Variablen. Wenn der Filter Frames löscht, aktualisiert er diesen Wert, indem die Dauer der einzelnen Frames subtrahiert wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Vtrans.h (einschließlich Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CVideoTransformFilter-Klasse**](cvideotransformfilter.md)
</dt> </dl>

 

 




