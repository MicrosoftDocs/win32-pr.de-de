---
description: 'Die advianperiodische-Methode erstellt eine regelmäßige anforderungsanforderung. Diese Methode implementiert die IReferenceClock:: advienperiodische-Methode.'
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Cbasereferenceclock. advianperiodische Methode (Ref. h)
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
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370223"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a>Cbasereferenceclock. advisperiodische-Methode

Die- `AdvisePeriodic` Methode erstellt eine regelmäßige anforderungsanforderung. Diese Methode implementiert die [**IReferenceClock:: advienperiodische**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) -Methode.

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

Zeitpunkt der ersten Benachrichtigung in 100-Nanosecond-Einheiten. Muss größer als 0 (null) und kleiner als die maximale \_ Zeit sein.

</dd> <dt>

*Periodtime* 
</dt> <dd>

Zeit zwischen Benachrichtigungen in 100-Nanosecond-Einheiten. Muss größer sein als Null.

</dd> <dt>

*hsemaphore* 
</dt> <dd>

Handle für ein Semaphor, das vom Aufrufer erstellt wurde.

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

Bei jeder Benachrichtigungs Zeit gibt die Uhr das im *hsemaphore* -Parameter angegebene Semaphor frei. Wenn keine weiteren Benachrichtigungen erforderlich sind, wenden Sie die [**cbasereferenceclock:: unadvi-Methode**](cbasereferenceclock-unadvise.md) an, und übergeben Sie den von diesem-Befehl zurückgegebenen *pdwadvistoken* -Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ref. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasereferenceclock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




