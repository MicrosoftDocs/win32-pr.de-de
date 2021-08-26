---
description: 'CBasePin.EnumMediaTypes-Methode: Die EnumMediaTypes-Methode listet die bevorzugten Medientypen des Pins auf. Diese Methode implementiert die IPin::EnumMediaTypes-Methode.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: CBasePin.EnumMediaTypes-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95c79071030b2f40613138e526abd1f965d3b5aeb7b233c2c53be57b65f97da7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916400"
---
# <a name="cbasepinenummediatypes-method"></a>CBasePin.EnumMediaTypes-Methode

Die `EnumMediaTypes` -Methode listet die bevorzugten Medientypen des Pins auf. Diese Methode implementiert die [**IPin::EnumMediaTypes-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppEnum* 
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IEnumMediaTypes-Schnittstelle empfängt.**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                                   | Beschreibung                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>       |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | **NULL-Zeigerargument.**<br/> |



 

## <a name="remarks"></a>Hinweise

Eingabepins sind nicht erforderlich, um bevorzugte Typen aufzuzählen. Ausgabepins müssen mindestens einen bevorzugten Typ aufzählen. Andernfalls könnten beide Pins einen bevorzugten Typ aufweisen, wodurch eine Verbindung unmöglich wird.

Die **IEnumMediaTypes-Schnittstelle** funktioniert wie ein COM-Standardenumerator. Weitere Informationen finden Sie unter [Aufzählen von Objekten in einem Filter Graph](enumerating-objects-in-a-filter-graph.md). Wenn die Methode erfolgreich ist, verfügt die **IEnumMediaTypes-Schnittstelle** über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie es freigeben, wenn Sie fertig sind.

Die [**CEnumMediaTypes-Basisklasse**](cenummediatypes.md) implementiert **IEnumMediaTypes.** Sie ruft die [**CBasePin::GetMediaType-Methode**](cbasepin-getmediatype.md) des Pins auf, um die Medientypen aufzuzählen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




