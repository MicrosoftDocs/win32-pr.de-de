---
description: 'CBasePin.GetMediaType-Methode: Die GetMediaType-Methode ruft einen bevorzugten Medientyp nach Indexwert ab.'
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: CBasePin.GetMediaType-Methode (Amfilter.h)
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
ms.openlocfilehash: cc202c3b6dbc570d063ef74619b266c2faa20cb74322b29e61626418412e2cb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044080"
---
# <a name="cbasepingetmediatype-method"></a>CBasePin.GetMediaType-Methode

Die `GetMediaType` -Methode ruft einen bevorzugten Medientyp nach Indexwert ab.

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

Nullbasierter Indexwert.

</dd> <dt>

*pMediaType* 
</dt> <dd>

Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                                            | Beschreibung                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ S KEINE ELEMENTE \_ \_ \_ MEHR**</dt> </dl> | Index liegt nicht im Bereich.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Index kleiner als 0 (null).<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>           | Unerwarteter Fehler.<br/>     |



 

## <a name="remarks"></a>Hinweise

Aus der Liste der bevorzugten Medientypen des Pins gibt diese Methode den Typ mit dem Indexwert *iPosition zurück.* Die [**CEnumMediaTypes-Klasse**](cenummediatypes.md) ruft diese Methode auf, um bevorzugte Medientypen aufzählen.

Die Basisklasse gibt E \_ UNEXPECTED zurück. Überschreiben Sie diese Methode in der abgeleiteten Klasse.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




