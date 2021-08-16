---
description: Die Run-Methode führt das -Objekt aus. Diese Methode implementiert die IMediaFilter::Run-Methode.
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: CBaseMediaFilter.Run-Methode (Amfilter.h)
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
ms.openlocfilehash: 73ab65404b6946a1cf220db54789df1234e14bf815c44633d3237ab50e04e2e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823690"
---
# <a name="cbasemediafilterrun-method"></a>CBaseMediaFilter.Run-Methode

Die `Run` -Methode führt das -Objekt aus. Diese Methode implementiert die [**IMediaFilter::Run-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)

## <a name="syntax"></a>Syntax


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tStart* 
</dt> <dd>

Die Verweiszeit, die der Streamzeit 0 entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Wenn das Objekt beendet wird, hält diese Methode das Objekt an, indem die [**CBaseMediaFilter::P ause-Methode aufgerufen**](cbasemediafilter-pause.md) wird. Anschließend wird die [**CBaseMediaFilter::m \_ State-Membervariable**](cbasemediafilter-m-state.md) auf State Running (Wird ausgeführt) \_ fest.

Die Streamzeit wird als aktuelle Referenzzeit minus *tStart berechnet.* Ein Medienbeispiel mit einem Zeitstempel von 0 (null) sollte zum Zeitpunkt *tStart gerendert werden.*

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseMediaFilter-Klasse**](cbasemediafilter.md)
</dt> </dl>

 

 




