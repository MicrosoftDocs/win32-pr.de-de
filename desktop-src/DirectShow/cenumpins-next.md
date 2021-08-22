---
description: Die Next-Methode ruft eine angegebene Anzahl von Pins in der Enumerationssequenz ab. Diese Methode implementiert die IEnumPins::Next-Methode.
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: CEnumPins.Next-Methode (Amfilter.h)
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
ms.openlocfilehash: 683b8eb5beb9946db7f37d4db53a84c96d5bff7fc91fa4864020fffde5554824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567080"
---
# <a name="cenumpinsnext-method"></a>CEnumPins.Next-Methode

Die Next-Methode ruft eine angegebene Anzahl von Pins in der Enumerationssequenz ab. Diese Methode implementiert die [**IEnumPins::Next-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next)

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

*cPins* 
</dt> <dd>

Anzahl der abzurufenden Pins.

</dd> <dt>

*ppPins* 
</dt> <dd>

Array der Größe *cPins,* das mit [**IPin-Zeigern**](/windows/desktop/api/Strmif/nn-strmif-ipin) gefüllt ist.

</dd> <dt>

*pcFetched* 
</dt> <dd>

Zeiger auf eine Variable, die die Anzahl der abgerufenen Pins empfängt. Kann **NULL** sein, wenn *cPins* 1 ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                | Beschreibung                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Es wurden nicht so viele Pins wie angefordert abgerufen.<br/>                                 |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Erfolg.<br/>                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Ungültiges Argument.<br/>                                                           |
| <dl> <dt>**E \_ POINTER**</dt> </dl>                  | **NULL-Zeigerargument.**<br/>                                                  |
| <dl> <dt>**VFW \_ E \_ ENUM \_ OUT \_ OF \_ SYNC**</dt> </dl> | Der Status des Filters hat sich geändert und ist nun mit dem Enumerator inkonsistent.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft Zeiger auf die angegebene Anzahl von Pins ab, beginnend an der aktuellen Position in der Enumeration, und platziert sie im angegebenen Array.

Diese Methode ruft die [**CBaseFilter::GetPin-Methode**](cbasefilter-getpin.md) des Filters auf, um die Pins abzurufen.

Wenn die Methode erfolgreich ist, verfügen alle **IPin-Zeiger** über ausstehende Verweisanzahlen. Stellen Sie sicher, dass Sie sie freigeben, wenn Sie fertig sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CEnumPins-Klasse**](cenumpins.md)
</dt> </dl>

 

 




