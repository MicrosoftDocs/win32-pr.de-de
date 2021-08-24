---
description: Die Set-Methode signalisiert das Ereignis.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: WEBCAMEvent.Set-Methode (Wxutil.h)
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
ms.openlocfilehash: 84059a66a77744b7ea570473474f6b773beae8005b7c4a68e73e59c76829f13a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794280"
---
# <a name="cameventset-method"></a>CAMEvent.Set-Methode

Die `Set` -Methode signalisiert das -Ereignis.

## <a name="syntax"></a>Syntax


```C++
void Set();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das Verhalten hängt davon ab, ob das Objekt ein Ereignis für die automatische Zurücksetzung oder ein Manuelles Zurücksetzen ist:

-   **Automatisches Zurücksetzen:** Wenn Threads auf dieses Ereignis warten, wird ein Thread freigegeben, und das Ereignis wird zurückgesetzt. Wenn keine Threads auf dieses Ereignis warten, bleibt das Ereignis signalisiert.
-   **Manuelles Zurücksetzen:** Alle Threads, die auf dieses Ereignis warten, werden freigegeben. Das Ereignis bleibt signalisiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CAMEvent-Klasse**](camevent.md)
</dt> </dl>

 

 




