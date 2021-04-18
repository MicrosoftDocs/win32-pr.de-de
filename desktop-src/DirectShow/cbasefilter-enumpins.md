---
description: 'Die Methode umumpins listet die Pins für diesen Filter auf. Diese Methode implementiert die ibasefilter:: umumpins-Methode.'
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: Cbasefilter. endumpins-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.EnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66a0f88a9749ba1dabb982e2f275da8a4be2a422
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360928"
---
# <a name="cbasefilterenumpins-method"></a>Cbasefilter. endumpins-Methode

Die- `EnumPins` Methode listet die Pins für diesen Filter auf. Diese Methode implementiert die [**ibasefilter:: umumpins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumPins(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnum* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**iumumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück.



| Rückgabecode                                                                                   | Beschreibung                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>                   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher<br/>       |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | **Null** -Zeigerargument<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode erstellt eine Instanz der [**cenumpins**](cenumpins.md) -Basisklasse und gibt einen Zeiger auf dieses Objekt vom Typ **ienumpins** zurück. Die **cenumpins** -Klasse ruft die [**cbasefilter:: getpin**](cbasefilter-getpin.md) -Methode des Filters auf, um die Pins für den Filter aufzuzählen.

Wenn diese Methode erfolgreich ausgeführt wird, hat die **ieinumpins** -Schnittstelle einen ausstehenden Verweis Zähler. Der Aufrufer muss die-Schnittstelle freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




