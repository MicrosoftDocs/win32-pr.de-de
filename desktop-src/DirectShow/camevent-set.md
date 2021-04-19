---
description: Die Set-Methode signalisiert das-Ereignis.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: Camevent. Set-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9caeed17d42d121ae9263bf6c1fcd011ed573c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366835"
---
# <a name="cameventset-method"></a>Camevent. Set-Methode

Die- `Set` Methode signalisiert das-Ereignis.

## <a name="syntax"></a>Syntax


```C++
void Set();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das Verhalten hängt davon ab, ob es sich bei dem Objekt um ein Auto Reset-Ereignis oder ein manuelles Zurücksetzungs Ereignis handelt:

-   **Automatisch zurückgesetzt**: Wenn Threads auf dieses Ereignis warten, wird ein Thread freigegeben, und das Ereignis wird zurückgesetzt. Wenn keine Threads auf dieses Ereignis warten, bleibt das Ereignis signalisiert.
-   **Manuelles Zurücksetzen**: alle Threads, die auf dieses Ereignis warten, werden freigegeben. Das Ereignis bleibt signalisiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camevent-Klasse**](camevent.md)
</dt> </dl>

 

 




