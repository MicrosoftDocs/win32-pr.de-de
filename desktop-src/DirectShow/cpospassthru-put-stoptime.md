---
description: Die \_ put StopTime-Methode legt die Zeit fest, zu der die Wiedergabe beendet wird, relativ zur Dauer des Streams. Diese Methode implementiert die IMediaPosition::p ut \_ StopTime-Methode.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: CPosPassThru.put_StopTime-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d91d49f2517a3d3b9efc50d70ace1b75562b50df8acda7c48826e7c088439928
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055090"
---
# <a name="cpospassthruput_stoptime-method"></a>CPosPassThru.put \_ StopTime-Methode

Die `put_StopTime` -Methode legt die Zeit fest, zu der die Wiedergabe beendet wird, relativ zur Dauer des Streams. Diese Methode implementiert die [**IMediaPosition::p ut \_ StopTime-Methode.**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime)

## <a name="syntax"></a>Syntax


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*llTime* 
</dt> <dd>

Beendigungszeit als **Double-Wert** in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




