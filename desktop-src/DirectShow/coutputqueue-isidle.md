---
description: Die IsIdle-Methode bestimmt, ob das Objekt auf Daten wartet.
ms.assetid: be1b5633-f9e9-497e-8b6f-5634eae91273
title: COutputQueue.IsIdle-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsIdle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c231e6e9dac3e05be6c01a2f3ebd87b5cdd69b8822a5ce26f930277c457206c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652120"
---
# <a name="coutputqueueisidle-method"></a>COutputQueue.IsIdle-Methode

Die `IsIdle` -Methode bestimmt, ob das Objekt auf Daten wartet.

## <a name="syntax"></a>Syntax


```C++
BOOL IsIdle();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn der Thread wartet und das Beispielarray leer ist. Andernfalls wird **FALSE zurückgegeben.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




