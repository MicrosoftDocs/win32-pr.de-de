---
description: Die put \_ CurrentPosition-Methode legt die aktuelle Position relativ zur Gesamtdauer des Streams fest. Diese Methode implementiert die IMediaPosition::p \_ currentPosition-Methode.
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: CPosPassThru.put_CurrentPosition -Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab6a8323023e9a2cd20f9453dc00e0c56a688086f10772b72b59b3c012a24702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909220"
---
# <a name="cpospassthruput_currentposition-method"></a>CPosPassThru.put \_ CurrentPosition-Methode

Die `put_CurrentPosition` -Methode legt die aktuelle Position relativ zur Gesamtdauer des Streams fest. Diese Methode implementiert die [**IMediaPosition::p \_ currentPosition-Methode.**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition)

## <a name="syntax"></a>Syntax


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*llTime* 
</dt> <dd>

Neue Position in Sekunden.

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

 

 




