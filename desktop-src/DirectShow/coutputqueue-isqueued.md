---
description: Die IsQueued-Methode bestimmt, ob das Objekt einen Arbeitsthread verwendet, um Beispiele zu liefern.
ms.assetid: 8d26661f-6cd7-42ea-bc4b-8746d22a7ca0
title: COutputQueue.IsQueued-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsQueued
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e261127e16cd1190fb711d81a9f5fd5606738b7f9a3f8697902170662b99f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813580"
---
# <a name="coutputqueueisqueued-method"></a>COutputQueue.IsQueued-Methode

Die `IsQueued` -Methode bestimmt, ob das -Objekt einen Arbeitsthread verwendet, um Beispiele zu liefern.

## <a name="syntax"></a>Syntax


```C++
BOOL IsQueued();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn das Objekt einen Arbeitsthread verwendet, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




