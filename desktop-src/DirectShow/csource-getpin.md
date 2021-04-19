---
description: 'Die getpin-Methode ruft eine PIN ab. Diese Methode implementiert die rein virtuelle cbasefilter:: getpin-Methode.'
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: CSource. getpin-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11ff79c9d2d535a3370183b7f36bae25c5e1383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370041"
---
# <a name="csourcegetpin-method"></a>CSource. getpin-Methode

Die- `GetPin` Methode ruft eine PIN ab. Diese Methode implementiert die rein virtuelle [**cbasefilter:: getpin**](cbasefilter-getpin.md) -Methode.

## <a name="syntax"></a>Syntax


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*n* 
</dt> <dd>

Die Nummer der angegebenen PIN.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Zeiger auf das [**cbasepin**](cbasepin.md) -Objekt zurück, das die PIN implementiert, oder **null** , wenn der Index außerhalb des gültigen Bereichs liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSource-Klasse**](csource.md)
</dt> </dl>

 

 




