---
description: 'Die Run-Methode führt das-Objekt aus. Diese Methode implementiert die imediafilter:: Run-Methode.'
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: Cbasemediafilter. Run-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369956"
---
# <a name="cbasemediafilterrun-method"></a>Cbasemediafilter. Run-Methode

Die- `Run` Methode führt das-Objekt aus. Diese Methode implementiert die [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tSTART* 
</dt> <dd>

Verweis Zeit entsprechend der streamzeit 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Wenn das-Objekt beendet wird, hält diese Methode das-Objekt an, indem die [**cbasemediafilter::P ause**](cbasemediafilter-pause.md) -Methode aufgerufen wird. Anschließend wird die Variable [**cbasemediafilter:: m \_ State**](cbasemediafilter-m-state.md) Member auf State Running festgelegt \_ .

Die streamzeit wird als aktuelle Verweis Zeit abzüglich *tSTART* berechnet. Ein Medien Beispiel mit einem Zeitstempel von NULL sollte zum Zeitpunkt *tSTART* gerendert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasemediafilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




