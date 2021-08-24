---
description: Die Run-Methode führt den Filter aus. Diese Methode implementiert die IMediaFilter::Run-Methode.
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: CBaseFilter.Run-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6259e6ce00b0a2f93e0b71d6b44d1c6ed4aa65eaadca21ed0a78f1d16d98a42b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793280"
---
# <a name="cbasefilterrun-method"></a>CBaseFilter.Run-Methode

Die `Run` -Methode führt den Filter aus. Diese Methode implementiert die [**IMediaFilter::Run-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)

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

Gibt S \_ OK zurück, wenn erfolgreich, oder ein **HRESULT-Wert,** der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

Wenn der Filter beendet wird, hält diese Methode den Filter an, indem die [**CBaseFilter::P ause-Methode aufgerufen**](cbasefilter-pause.md) wird. Anschließend wird die [**CBasePin::Run-Methode**](cbasepin-run.md) für jeden verbundenen Pin des Filters aufruft. Schließlich wird die [**CBaseFilter::m \_ State-Membervariable**](cbasefilter-m-state.md) auf State \_ Running (Status wird ausgeführt) fest.

Die Streamzeit wird als aktuelle Referenzzeit minus *tStart berechnet.* Ein Medienbeispiel mit einem Zeitstempel von 0 (null) sollte zum Zeitpunkt *tStart gerendert werden.*

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




