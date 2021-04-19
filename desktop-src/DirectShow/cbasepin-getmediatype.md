---
description: Die getmediatype-Methode ruft einen bevorzugten Medientyp nach Indexwert ab.
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Cbasepin. getmediatype-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c54c5cd769a8efa0c720c7050cca45b00b8209e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372763"
---
# <a name="cbasepingetmediatype-method"></a>Cbasepin. getmediatype-Methode

Die- `GetMediaType` Methode ruft einen bevorzugten Medientyp nach Indexwert ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iPosition* 
</dt> <dd>

NULL basierter Indexwert.

</dd> <dt>

*pmediatype* 
</dt> <dd>

Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                            | Beschreibung                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ S \_ keine \_ weiteren \_ Elemente**</dt> </dl> | Der Index liegt außerhalb des zulässigen Bereichs.<br/>   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>           | Index kleiner als 0 (null).<br/> |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>           | Unerwarteter Fehler.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

In der Liste der bevorzugten Medientypen der PIN gibt diese Methode den Typ mit dem Indexwert *iPosition* zurück. Die [**cenummediatypes**](cenummediatypes.md) -Klasse ruft diese Methode auf, um bevorzugte Medientypen aufzuzählen.

Die Basisklasse gibt "E unerwartete" zurück \_ . Überschreiben Sie diese Methode in der abgeleiteten Klasse.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




