---
description: Die IncrementTypeVersion-Methode erhöht die Versionsnummer für den Satz bevorzugter Medientypen.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: CBasePin.IncrementTypeVersion-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a8c2536b91d5630141e5a62fa1aa895555537b61f89a574f4cdc1ec208810c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526860"
---
# <a name="cbasepinincrementtypeversion-method"></a>CBasePin.IncrementTypeVersion-Methode

Die `IncrementTypeVersion` -Methode erhöht die Versionsnummer für den Satz bevorzugter Medientypen.

## <a name="syntax"></a>Syntax


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode erhöht die [**CBasePin::m \_ TypeVersion-Membervariable.**](cbasepin-m-typeversion.md) Wenn der Pin die Liste der bevorzugten Medientypen dynamisch ändert, rufen Sie diese Methode auf, wenn sich die Liste ändert. Weitere Informationen finden Sie unter [**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




