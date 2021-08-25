---
description: Die put \_ PrerollTime-Methode legt die Menge der Daten fest, die vor der Startposition in die Warteschlange gestellt werden. Diese Methode implementiert die IMediaPosition::p ut \_ PrerollTime-Methode.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: CPosPassThru.put_PrerollTime -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825c3c584fc6db7eb9f94b4e8d01e003f5cf6c36ff8adac4041fd48f792ca858
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909200"
---
# <a name="cpospassthruput_prerolltime-method"></a>CPosPassThru.put \_ PrerollTime-Methode

Die `put_PrerollTime` -Methode legt die Datenmenge fest, die vor der Startposition in die Warteschlange gestellt wird. Diese Methode implementiert die [**IMediaPosition::p ut \_ PrerollTime-Methode.**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime)

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*llTime* 
</dt> <dd>

Vorabrollzeit in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** vom verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




