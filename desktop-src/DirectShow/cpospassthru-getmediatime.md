---
description: 'CPosPassThru.GetMediaTime-Methode: Die GetMediaTime-Methode ruft die Zeitstempel für das aktuelle Beispiel ab.'
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: CPosPassThru.GetMediaTime-Methode (Ctlutil.h)
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
ms.openlocfilehash: 328a0ae09c80a687863cfedb994f5a80cebebf14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095258"
---
# <a name="cpospassthrugetmediatime-method"></a>CPosPassThru.GetMediaTime-Methode

Die `GetMediaTime` -Methode ruft die Zeitstempel für das aktuelle Beispiel ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStartTime* 
</dt> <dd>

Zeiger auf eine Variable, die die Startzeit in Einheiten des aktuellen Zeitformats empfängt.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Zeiger auf eine Variable, die die Endzeit in Einheiten des aktuellen Zeitformats empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ FAIL zurück.

## <a name="remarks"></a>Bemerkungen

Überschreiben Sie diese Methode, wenn Ihr Filter die Zeitstempel für die empfangenen Beispiele zwischenspeichert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




