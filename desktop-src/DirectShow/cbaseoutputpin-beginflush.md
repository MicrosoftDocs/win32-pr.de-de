---
description: 'Die beginflush-Methode startet einen Löschvorgang. Implementiert die IPin:: beginflush-Methode.'
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Cbaseoutputpin. beginflush-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0216f74094d0c024d9b354dc594ff8d65315efbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371178"
---
# <a name="cbaseoutputpinbeginflush-method"></a>Cbaseoutputpin. beginflush-Methode

Die- `BeginFlush` Methode startet einen Löschvorgang. Implementiert die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginFlush();
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

 

 




