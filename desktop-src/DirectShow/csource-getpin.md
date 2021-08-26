---
description: Die GetPin-Methode ruft eine Stecknadel ab. Diese Methode implementiert die rein virtuelle CBaseFilter::GetPin-Methode.
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: CSource.GetPin-Methode (Source.h)
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
ms.openlocfilehash: 4c5b7548eca20f9ec6d9e03d0e708ead1b106f543ca8cac108700c64c9352ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087080"
---
# <a name="csourcegetpin-method"></a>CSource.GetPin-Methode

Die `GetPin` -Methode ruft einen Pin ab. Diese Methode implementiert die rein virtuelle [**CBaseFilter::GetPin-Methode.**](cbasefilter-getpin.md)

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

Nummer des angegebenen Pins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Zeiger auf das [**CBasePin-Objekt**](cbasepin.md) zurück, das den Pin implementiert, oder **NULL,** wenn der Index außerhalb des Zulässigkeitsbereichs liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSource-Klasse**](csource.md)
</dt> </dl>

 

 




