---
description: Die EnumPins-Methode listet die Pins für diesen Filter auf. Diese Methode implementiert die IBaseFilter::EnumPins-Methode.
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: CBaseFilter.EnumPins-Methode (Amfilter.h)
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
ms.openlocfilehash: 3cd0be44f768898a530eef20d3e4d5d082d230ff809133c0eb62ceb2308b524b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640580"
---
# <a name="cbasefilterenumpins-method"></a>CBaseFilter.EnumPins-Methode

Die `EnumPins` -Methode listet die Stecknadeln für diesen Filter auf. Diese Methode implementiert die [**IBaseFilter::EnumPins-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins)

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

Adresse einer Variablen, die einen Zeiger auf die [**IEnumPins-Schnittstelle empfängt.**](/windows/desktop/api/Strmif/nn-strmif-ienumpins)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück.



| Rückgabecode                                                                                   | Beschreibung                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher<br/>       |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | **NULL-Zeigerargument**<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode erstellt eine Instanz der [**CEnumPins-Basisklasse**](cenumpins.md) und gibt einen Zeiger auf dieses Objekt vom Typ **IEnumPins** zurück. Die **CEnumPins-Klasse** ruft die [**CBaseFilter::GetPin-Methode**](cbasefilter-getpin.md) des Filters auf, um die Pins für den Filter aufzuzählen.

Wenn diese Methode erfolgreich ist, verfügt die **IEnumPins-Schnittstelle** über einen ausstehenden Verweiszähler. Der Aufrufer muss die Schnittstelle freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




