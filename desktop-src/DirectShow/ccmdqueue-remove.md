---
description: Die Remove-Methode entfernt das CDeferredCommand-Objekt aus der Warteschlange.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: CCmdQueue.Remove-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d0b0a4b416c5adb97b1a9efba1fbd5f6142b0e0fb761c6d4c0b277ac0cda7e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954579"
---
# <a name="ccmdqueueremove-method"></a>CCmdQueue.Remove-Methode

Die `Remove` -Methode entfernt das [**CDeferredCommand-Objekt**](cdeferredcommand.md) aus der Warteschlange.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCmd* 
</dt> <dd>

Zeiger auf das **CDeferredCommand-Objekt,** das aus der Warteschlange entfernt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt VFW \_ E \_ NOT FOUND \_ zurück, wenn das Objekt nicht in der Warteschlange gefunden wurde. Andernfalls gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CCmdQueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




