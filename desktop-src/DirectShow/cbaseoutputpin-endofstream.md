---
description: 'CBaseOutputPin.EndOfStream-Methode: Die EndOfStream-Methode benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden. Diese Methode implementiert die IPin::EndOfStream-Methode.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: CBaseOutputPin.EndOfStream-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93ba617ddb061a928236e9bbf7d7a411812809092efa8a71f5890ddeecb88328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823599"
---
# <a name="cbaseoutputpinendofstream-method"></a>CBaseOutputPin.EndOfStream-Methode

Die `EndOfStream` -Methode benachrichtigt den Pin, dass keine zusätzlichen Daten erwartet werden. Diese Methode implementiert die [**IPin::EndOfStream-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)

## <a name="syntax"></a>Syntax


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt E \_ UNEXPECTED zurück.

## <a name="remarks"></a>Hinweise

Diese Methode sollte nur für Eingabepins aufgerufen werden, sodass die **CBaseOutputPin-Implementierung** E \_ UNEXPECTED zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




