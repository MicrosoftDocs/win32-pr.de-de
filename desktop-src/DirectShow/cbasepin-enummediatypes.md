---
description: 'Die enummediatypes-Methode listet die bevorzugten Medientypen der PIN auf. Diese Methode implementiert die IPin:: enummediatypes-Methode.'
ms.assetid: 0360f9fc-6876-4a54-8de1-bf289e0e10ae
title: Cbasepin. enummediatypes-Methode (amfilter. h)
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
ms.openlocfilehash: 54aaddbbcde26791b6c55665bfbbb7ff62048238
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372427"
---
# <a name="cbasepinenummediatypes-method"></a>Cbasepin. enummediatypes-Methode

Die `EnumMediaTypes` -Methode listet die bevorzugten Medientypen der PIN auf. Diese Methode implementiert die [**IPin:: enummediatypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) -Methode.

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

Adresse einer Variablen, die einen Zeiger auf die [**ienummediatypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) -Schnittstelle empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                   | Beschreibung                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>       |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | **Null** -Zeigerargument.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Eingabe Pins sind nicht erforderlich, um bevorzugte Typen aufzuzählen. Ausgabe Pins müssen mindestens einen bevorzugten Typ auflisten. Andernfalls könnten beide Pins einen bevorzugten Typ haben und eine Verbindung unmöglich machen.

Die **ienummediatypes** -Schnittstelle funktioniert wie ein Standard-com-Enumerator. Weitere Informationen finden Sie unter Auflisten von [Objekten in einem Filter Diagramm](enumerating-objects-in-a-filter-graph.md). Wenn die Methode erfolgreich ausgeführt wird, hat die **ienummediatypes** -Schnittstelle einen ausstehenden Verweis Zähler. Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.

Die [**cenummediatypes**](cenummediatypes.md) -Basisklasse implementiert **ienummediatypes**. Sie ruft die [**cbasepin:: getmediatype**](cbasepin-getmediatype.md) -Methode der PIN auf, um die Medientypen aufzuzählen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




