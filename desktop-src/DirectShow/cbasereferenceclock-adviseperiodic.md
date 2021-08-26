---
description: Die AdvisePeriodic-Methode erstellt eine regelmäßige Empfehlungsanforderung. Diese Methode implementiert die IReferenceClock::AdvisePeriodic-Methode.
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: CBaseReferenceClock.AdvisePeriodic-Methode (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4b81fc8dfc33cc2a6e5207e984de0c2e693b8c00b8f8d35949d0bb7150484bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052430"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a>CBaseReferenceClock.AdvisePeriodic-Methode

Die `AdvisePeriodic` -Methode erstellt eine regelmäßige Empfehlungsanforderung. Diese Methode implementiert die [**IReferenceClock::AdvisePeriodic-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic)

## <a name="syntax"></a>Syntax


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartTime* 
</dt> <dd>

Zeitpunkt der ersten Benachrichtigung in Einheiten von 100 Nanosekunden. Muss größer als 0 (null) und kleiner als MAX \_ TIME sein.

</dd> <dt>

*PeriodTime* 
</dt> <dd>

Zeit zwischen Benachrichtigungen in Einheiten von 100 Nanosekunden. Muss größer sein als Null.

</dd> <dt>

*hSemaphore* 
</dt> <dd>

Handle für ein vom Aufrufer erstelltes Semaphor.

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

Zu jeder Benachrichtigungszeit gibt die Uhr das im *hSemaphore-Parameter* angegebene Semaphor frei. Wenn keine weiteren Benachrichtigungen erforderlich sind, rufen Sie die [**CBaseReferenceClock::Unadvise-Methode**](cbasereferenceclock-unadvise.md) auf, und übergeben Sie den *pdwAdviseToken-Wert,* der von diesem Aufruf zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Refclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseReferenceClock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




