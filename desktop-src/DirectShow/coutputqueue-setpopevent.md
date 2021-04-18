---
description: Die setpopevent-Methode gibt ein Ereignis an, das signalisiert wird, wenn das Objekt ein Beispiel aus der Warteschlange entfernt.
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: Coutputqueue. setpopevent-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365913"
---
# <a name="coutputqueuesetpopevent-method"></a>Coutputqueue. setpopevent-Methode

Die- `SetPopEvent` Methode gibt ein Ereignis an, das signalisiert wird, wenn das Objekt ein Beispiel aus der Warteschlange entfernt.

## <a name="syntax"></a>Syntax


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hevent* 
</dt> <dd>

Handle für ein Ereignis, das vom Aufrufer erstellt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




