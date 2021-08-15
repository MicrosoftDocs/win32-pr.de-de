---
description: Die GetSchedule-Methode ruft einen Zeiger auf das Zeitplanungsobjekt der Uhr ab.
ms.assetid: ae509f16-d85f-4365-8cf2-c6585cbbdc3d
title: CBaseReferenceClock.GetSchedule-Methode (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6be5c4ed76573428967138682b478a54859e4ca97213f132ff805a0e83be0b50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822836"
---
# <a name="cbasereferenceclockgetschedule-method"></a>CBaseReferenceClock.GetSchedule-Methode

Die `GetSchedule` -Methode ruft einen Zeiger auf das Zeitplanungsobjekt der Uhr ab.

## <a name="syntax"></a>Syntax


```C++
CAMSchedule* GetSchedule();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die [**CBaseReferenceClock::m \_ pSchedule-Membervariable**](cbasereferenceclock-m-pschedule.md) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Refclock.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseReferenceClock-Klasse**](cbasereferenceclock.md)
</dt> </dl>

 

 




