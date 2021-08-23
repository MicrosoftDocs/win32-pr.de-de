---
description: Die BeginFlush-Methode startet einen Leerungsvorgang. Implementiert die IPin::BeginFlush-Methode.
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: CBaseOutputPin.BeginFlush-Methode (Amfilter.h)
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
ms.openlocfilehash: 5dd12216fb040601d73eb566d47ec5c8c3ceeec685bd8f7abc6877756f94c6a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640010"
---
# <a name="cbaseoutputpinbeginflush-method"></a>CBaseOutputPin.BeginFlush-Methode

Die `BeginFlush` -Methode startet einen Leerungsvorgang. Implementiert die [**IPin::BeginFlush-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)

## <a name="syntax"></a>Syntax


```C++
HRESULT BeginFlush();
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




