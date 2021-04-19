---
description: 'Die GetClassID-Methode ruft den Klassen Bezeichner ab. Diese Methode implementiert die ipersistent:: GetClassID-Methode.'
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: Cbasemediafilter. GetClassID-Methode (amfilter. h)
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
ms.openlocfilehash: 4dafacba684711c5c04a155d2609e0bc68450fa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369421"
---
# <a name="cbasemediafiltergetclassid-method"></a>Cbasemediafilter. GetClassID-Methode

Die- `GetClassID` Methode ruft den Klassen Bezeichner ab. Diese Methode implementiert die **ipersistent:: GetClassID-** Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pclsid* 
</dt> <dd>

Ein Zeiger auf eine Variable, die den Klassen Bezeichner empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den S \_ OK-oder E- \_ Zeiger zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasemediafilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




