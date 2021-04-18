---
description: Die Remove-Methode entfernt das cdeferredcommand-Objekt aus der Warteschlange.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Ccmdqueue. Remove-Methode (winutil. h)
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
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364458"
---
# <a name="ccmdqueueremove-method"></a>Ccmdqueue. Remove-Methode

Die- `Remove` Methode entfernt das [**cdeferredcommand**](cdeferredcommand.md) -Objekt aus der Warteschlange.

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

Zeiger auf das **cdeferredcommand** -Objekt, das aus der Warteschlange entfernt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt VFW \_ E \_ nicht \_ gefunden zurück, wenn das Objekt in der Warteschlange nicht gefunden wurde. Andernfalls gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccmdqueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




