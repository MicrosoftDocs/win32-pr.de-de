---
description: Die getmediatime-Methode ruft die Zeitstempel im aktuellen Beispiel ab.
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Cpospassthru. getmediatime-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2748d986f121a38041155dcd43f13a647916486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364602"
---
# <a name="cpospassthrugetmediatime-method"></a>Cpospassthru. getmediatime-Methode

Die- `GetMediaTime` Methode ruft die Zeitstempel im aktuellen Beispiel ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pstarttime* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Startzeit in Einheiten des aktuellen Zeit Formats empfängt.

</dd> <dt>

*Zeit* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeit Formats empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "E Fail" zurück \_ .

## <a name="remarks"></a>Bemerkungen

Überschreiben Sie diese Methode, wenn der Filter die Zeitstempel der empfangenen Beispiele zwischenspeichert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




