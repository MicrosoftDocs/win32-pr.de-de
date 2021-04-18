---
description: 'Die Next-Methode ruft eine angegebene Anzahl von Pins in der enumerationssequenz ab. Diese Methode implementiert die iumumpins:: Next-Methode.'
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Cenumpins. Next-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 612dcd638939b34803b7296babf7445a07cdad22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365663"
---
# <a name="cenumpinsnext-method"></a>Cenumpins. Next-Methode

Die Next-Methode ruft eine angegebene Anzahl von Pins in der enumerationssequenz ab. Diese Methode implementiert die [**iumumpins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cpins* 
</dt> <dd>

Anzahl der abzurufenden Pins.

</dd> <dt>

*pppins* 
</dt> <dd>

Ein Array von Größen- *cpins* , das mit [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Zeigern gefüllt ist.

</dd> <dt>

*pcfetch* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der abgerufenen Pins empfängt. Kann **null** sein, wenn *cpins* den Wert 1 hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                                | Beschreibung                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                    | Es wurden nicht so viele Pins wie angefordert abgerufen.<br/>                                 |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                                                    |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>               | Ungültiges Argument.<br/>                                                           |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>                  | **Null** -Zeigerargument.<br/>                                                  |
| <dl> <dt>**VFW \_ E \_ Enum \_ nicht \_ \_ synchron**</dt> </dl> | Der Zustand des Filters wurde geändert und ist nun inkonsistent mit dem Enumerator.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft Zeiger auf die angegebene Anzahl von Pins ab, beginnend an der aktuellen Position in der Enumeration und platziert Sie im angegebenen Array.

Diese Methode ruft die [**cbasefilter:: getpin**](cbasefilter-getpin.md) -Methode des Filters auf, um die Pins abzurufen.

Wenn die Methode erfolgreich ausgeführt wird, weisen die **IPin** -Zeiger alle ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie Sie freigeben, wenn Sie dies erledigt haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cenumpins-Klasse**](cenumpins.md)
</dt> </dl>

 

 




