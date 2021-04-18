---
description: 'Die adviantime-Methode erstellt eine One-Shot-anforderungsanforderung. Diese Methode implementiert die IReferenceClock:: adviabtime-Methode.'
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Cbasereferenceclock. adviantime-Methode (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 326fc5e0939803ab66e0466fbf32351387977019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372158"
---
# <a name="cbasereferenceclockadvisetime-method"></a>Cbasereferenceclock. advientime-Methode

Die `AdviseTime` -Methode erstellt eine One-Shot-anforderungsanforderung. Diese Methode implementiert die [**IReferenceClock:: adviabtime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*baseTime* 
</dt> <dd>

Basis Verweis Zeit in 100-Nanosecond-Einheiten.

</dd> <dt>

*streamtime* 
</dt> <dd>

Streamoffset Zeit in 100-Nanosecond-Einheiten.

</dd> <dt>

*hevent* 
</dt> <dd>

Handle für ein Ereignis, das vom Aufrufer erstellt wurde.

</dd> <dt>

*pdwadvistoken* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Bezeichner für die Benachrichtigungs Anforderung empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                   | Beschreibung                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>                   |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültige Zeitwerte.<br/>       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Fehler<br/>                   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | **Null** -Zeigerargument<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode erstellt eine One-Shot-anforderungsanforderung für die Referenzzeit *baseTime*  +  *streamtime*. Die Summe muss größer als 0 (null) und kleiner als \_ die maximale Zeit sein, oder die Methode gibt E \_ invalidArg zurück. Die Uhr signalisiert zum angeforderten Zeitpunkt das Ereignis, das im *hevent* -Parameter angegeben ist.

Um die Benachrichtigung abzubrechen, bevor die Zeit erreicht ist, rufen Sie die [**cbasereferenceclock:: unadvi-Methode**](cbasereferenceclock-unadvise.md) auf, und übergeben Sie den von diesem Aufruf zurückgegebenen *pdwadvistoken* -Wert. Nachdem die Benachrichtigung erfolgt ist, wird Sie von der Uhr automatisch gelöscht. Daher ist es nicht erforderlich, die **Empfehlung "nicht empfohlen**" aufzurufen. Dies ist jedoch kein Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ref. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasereferenceclock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




