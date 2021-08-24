---
description: Die IsFlushing-Methode fragt ab, ob der Filter gerade geleert wird.
ms.assetid: 366b6162-7a2c-4882-8774-8b4bf83012b4
title: CBaseInputPin.IsFlushing-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.IsFlushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf14abbf20d01f5e78284b65dd1159202146437f2492423c2eaa998a65ee412f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017058"
---
# <a name="cbaseinputpinisflushing-method"></a>CBaseInputPin.IsFlushing-Methode

Die `IsFlushing` -Methode fragt ab, ob der Filter gerade geleert wird.

## <a name="syntax"></a>Syntax


```C++
BOOL IsFlushing();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die [**CBaseInputPin::m \_ bFlushing-Membervariable**](cbaseinputpin-m-bflushing.md) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseInputPin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




