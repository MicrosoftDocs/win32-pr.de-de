---
description: Die AdviseTime-Methode erstellt eine einmalige Empfehlungsanforderung. Diese Methode implementiert die IReferenceClock::AdviseTime-Methode.
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: CBaseReferenceClock.AdviseTime-Methode (Refclock.h)
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
ms.openlocfilehash: e50b864a63cdd021d82c0a2a73f4f9c3acb68d1afb1f6a2dcd8d8d575966a5fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502790"
---
# <a name="cbasereferenceclockadvisetime-method"></a>CBaseReferenceClock.AdviseTime-Methode

Die `AdviseTime` -Methode erstellt eine einmalige Empfehlungsanforderung. Diese Methode implementiert die [**IReferenceClock::AdviseTime-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime)

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

Basisreferenzzeit in Einheiten von 100 Nanosekunden.

</dd> <dt>

*streamTime* 
</dt> <dd>

Streamoffsetzeit in Einheiten von 100 Nanosekunden.

</dd> <dt>

*hEvent* 
</dt> <dd>

Behandeln sie mit einem Ereignis, das vom Aufrufer erstellt wurde.

</dd> <dt>

*pdwAdviseToken* 
</dt> <dd>

Zeiger auf eine Variable, die einen Bezeichner für die Empfehlungsanforderung empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Tabelle gezeigten **HRESULT-Werte** zurück.



| Rückgabecode                                                                                   | Beschreibung                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültige Zeitwerte<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Fehler<br/>                   |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | **NULL-Zeigerargument**<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode erstellt eine einmalige Empfehlungsanforderung für die *Referenzzeit baseTime*  +  *streamTime*. Die Summe muss größer als 0 (null) und kleiner als MAX \_ TIME sein, andernfalls gibt die Methode E \_ INVALIDARG zurück. Zum angeforderten Zeitpunkt signalisiert die Uhr das im *hEvent-Parameter* angegebene Ereignis.

Um die Benachrichtigung abzubrechen, bevor die Zeit erreicht ist, rufen Sie die [**CBaseReferenceClock::Unadvise-Methode**](cbasereferenceclock-unadvise.md) auf, und übergeben Sie den *pdwAdviseToken-Wert,* der von diesem Aufruf zurückgegeben wird. Nachdem die Benachrichtigung aufgetreten ist, löscht die Uhr sie automatisch, sodass es nicht erforderlich ist, **Unadvise** aufzurufen. Dies ist jedoch kein Fehler.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Refclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseReferenceClock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




