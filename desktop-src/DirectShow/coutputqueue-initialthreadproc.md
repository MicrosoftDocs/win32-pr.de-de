---
description: 'Die initialthread proc-Methode ruft die coutputqueue:: Thread proc-Methode auf, wenn der Thread erstellt wird.'
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.Initialthread proc-Methode (outputq. h)
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
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371271"
---
# <a name="coutputqueueinitialthreadproc-method"></a>COutputQueue.Initialthread proc-Methode

Die- `InitialThreadProc` Methode ruft die [**coutputqueue:: Thread proc**](coutputqueue-threadproc.md) -Methode auf, wenn der Thread erstellt wird.

## <a name="syntax"></a>Syntax


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*teuren* 
</dt> <dd>

`this` Zeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert zurück, der von der [**coutputqueue:: ThreadProc**](coutputqueue-threadproc.md) -Methode zurückgegeben wird.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist die Thread Prozedur für den Arbeits Thread des Objekts. Der Zeiger des Objekts `this` ist der Thread Parameter. Die-Methode dereferenziert dieses, um **ThreadProc** aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




