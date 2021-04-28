---
description: 'CBasePin.EnumMediaTypes-Methode: Die EnumMediaTypes-Methode aufzählt die bevorzugten Medientypen des Pins. Diese Methode implementiert die IPin::EnumMediaTypes-Methode.'
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
ms.openlocfilehash: c68fe1ab83724149dcd2fb58a60e9c6950d887ca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099388"
---
# <a name="cbasepinenummediatypes-method"></a>CBasePin.EnumMediaTypes-Methode

Die `EnumMediaTypes` -Methode aufzählt die bevorzugten Medientypen des Pins. Diese Methode implementiert die [**IPin::EnumMediaTypes-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)

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

Adresse einer Variablen, die einen Zeiger auf die [**IEnumMediaTypes-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                                   | Beschreibung                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>       |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>     |  NULL-Zeigerargument.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Eingabepins sind nicht erforderlich, um bevorzugte Typen aufzählen zu können. Ausgabepins müssen mindestens einen bevorzugten Typ aufzählen. Andernfalls könnten beide Stecknadeln keinen bevorzugten Typ haben, was eine Verbindung unmöglich macht.

Die **IEnumMediaTypes-Schnittstelle** funktioniert wie ein COM-Standardenumerator. Weitere Informationen finden Sie unter [Aufzählen von Objekten in einem Filterdiagramm.](enumerating-objects-in-a-filter-graph.md) Wenn die Methode erfolgreich ist, verfügt die **IEnumMediaTypes-Schnittstelle** über eine ausstehende Verweisanzahl. Stellen Sie sicher, dass Sie sie veröffentlichen, wenn Sie fertig sind.

Die [**CEnumMediaTypes-Basisklasse**](cenummediatypes.md) implementiert **IEnumMediaTypes.** Sie ruft die [**CBasePin::GetMediaType-Methode**](cbasepin-getmediatype.md) des Pins auf, um die Medientypen aufzuzählen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




