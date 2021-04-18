---
description: Die incrementtypeversion-Methode erhöht die Versionsnummer für den Satz bevorzugter Medientypen.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: Cbasepin. incrementtypeversion-Methode (amfilter. h)
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
ms.openlocfilehash: 6db3c08972bebbaf1172c44412ae9c8652100da8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371534"
---
# <a name="cbasepinincrementtypeversion-method"></a>Cbasepin. incrementtypeversion-Methode

Die- `IncrementTypeVersion` Methode erhöht die Versionsnummer für den Satz bevorzugter Medientypen.

## <a name="syntax"></a>Syntax


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode erhöht die Member-Variable [**cbasepin:: m \_ typeversion**](cbasepin-m-typeversion.md) . Wenn die PIN die Liste der bevorzugten Medientypen dynamisch ändert, wird diese Methode immer dann aufgerufen, wenn die Liste geändert wird. Weitere Informationen finden Sie unter [**cbasepin:: getmediatypeer Version**](cbasepin-getmediatypeversion.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




