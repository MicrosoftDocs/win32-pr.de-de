---
description: Die InitialThreadProc-Methode ruft die COutputQueue::ThreadProc-Methode auf, wenn der Thread erstellt wird.
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.InitialThreadProc-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a80561ae652df7168ad09c1cf6e9fde767154e6c72a8fe5360a5d09c784941f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813590"
---
# <a name="coutputqueueinitialthreadproc-method"></a>COutputQueue.InitialThreadProc-Methode

Die `InitialThreadProc` -Methode ruft die [**COutputQueue::ThreadProc-Methode**](coutputqueue-threadproc.md) auf, wenn der Thread erstellt wird.

## <a name="syntax"></a>Syntax


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pv* 
</dt> <dd>

`this` Zeiger.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den von der [**COutputQueue::ThreadProc-Methode**](coutputqueue-threadproc.md) zurückgegebenen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode ist die Threadprozedur für den Arbeitsthread des Objekts. Der Zeiger des Objekts `this` ist der Threadparameter. Die -Methode dereferenziert dies, um **ThreadProc** aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




