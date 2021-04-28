---
description: 'CBaseOutputPin.EndFlush-Methode: Die EndFlush-Methode beendet einen Leerungsvorgang. Diese Methode implementiert die IPin::EndFlush-Methode.'
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: CBaseOutputPin.EndFlush-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53153c6dbd941390c7ef616ee36c56e01214c341
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099508"
---
# <a name="cbaseoutputpinendflush-method"></a>CBaseOutputPin.EndFlush-Methode

Die `EndFlush` -Methode beendet einen Leerungsvorgang. Diese Methode implementiert die [**IPin::EndFlush-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)

## <a name="syntax"></a>Syntax


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt E \_ UNEXPECTED zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode sollte nur für Eingabepins aufgerufen werden, sodass die **CBaseOutputPin-Implementierung** E \_ UNEXPECTED zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (streams.h einschließen)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




