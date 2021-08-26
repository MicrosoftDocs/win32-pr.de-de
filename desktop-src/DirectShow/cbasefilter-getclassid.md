---
description: Die GetClassID-Methode ruft den Klassenbezeichner des Filters ab. Diese Methode implementiert die IPersist::GetClassID-Methode.
ms.assetid: c3a8b6ab-b36f-493e-9436-6784e25e2511
title: CBaseFilter.GetClassID-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 365c8b6d41231da78a1f478f998373247913e132c95b4c532c413f8080a2e362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056660"
---
# <a name="cbasefiltergetclassid-method"></a>CBaseFilter.GetClassID-Methode

Die `GetClassID` -Methode ruft den Klassenbezeichner des Filters ab. Diese Methode implementiert die **IPersist::GetClassID-Methode.**

## <a name="syntax"></a>Syntax


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pClsID* 
</dt> <dd>

Zeiger auf eine Variable, die den Klassenbezeichner empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E POINTER \_ zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




