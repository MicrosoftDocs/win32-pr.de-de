---
description: Die findi-Methode ruft die erste Position ab, die das angegebene Element enthält.
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: Cbaselist. findi-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2366f8c4c117b8550d91c84bffafb03393801088
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351344"
---
# <a name="cbaselistfindi-method"></a>Cbaselist. findi-Methode

Die- `FindI` Methode ruft die erste Position ab, die das angegebene Element enthält.

## <a name="syntax"></a>Syntax


```C++
POSITION FindI(
   void *pObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pobj* 
</dt> <dd>

Zeiger auf das Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Positionswert oder **null** zurück, wenn das Element nicht in der Liste enthalten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxlist. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaselist-Klasse**](cbaselist.md)
</dt> </dl>

 

 




