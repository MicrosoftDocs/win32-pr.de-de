---
description: 'Die EndOf-Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden. Diese Methode implementiert die IPin:: EndOf Stream-Methode.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: Cbaseoutputpin. EndOf Stream-Methode (amfilter. h)
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
ms.openlocfilehash: e1cd903e811dbcd000ba202fc86c0fcb41bf221b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354761"
---
# <a name="cbaseoutputpinendofstream-method"></a>Cbaseoutputpin. EndOf Stream-Methode

Die- `EndOfStream` Methode benachrichtigt die PIN, dass keine weiteren Daten erwartet werden. Diese Methode implementiert die [**IPin:: EndOf Stream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt "E unerwartete" zurück \_ .

## <a name="remarks"></a>Bemerkungen

Diese Methode sollte nur für Eingabe Pins aufgerufen werden, sodass die **cbaseoutputpin** -Implementierung E \_ unerwartet zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




