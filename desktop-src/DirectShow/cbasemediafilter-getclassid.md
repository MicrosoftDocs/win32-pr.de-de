---
description: Die GetClassID-Methode ruft den Klassenbezeichner ab. Diese Methode implementiert die IPersist::GetClassID-Methode.
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: CBaseMediaFilter.GetClassID-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a733c3ef6e7098a556facb5258f567bdae0179ba4da133076b9bbc961cf0b26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502920"
---
# <a name="cbasemediafiltergetclassid-method"></a>CBaseMediaFilter.GetClassID-Methode

Die `GetClassID` -Methode ruft den Klassenbezeichner ab. Diese Methode implementiert die **IPersist::GetClassID-Methode.**

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

Gibt S \_ OK oder E \_ POINTER zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseMediaFilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




