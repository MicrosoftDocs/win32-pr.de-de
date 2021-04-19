---
description: Die Insert-Methode fügt der Warteschlange ein cdeferredcommand-Objekt hinzu.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: Ccmdqueue. Insert-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369541"
---
# <a name="ccmdqueueinsert-method"></a>Ccmdqueue. Insert-Methode

Die- `Insert` Methode fügt der Warteschlange ein [**cdeferredcommand**](cdeferredcommand.md) -Objekt hinzu.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCmd* 
</dt> <dd>

Zeiger auf das **cdeferredcommand** -Objekt, das der Warteschlange hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK in der Standard Implementierung zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccmdqueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




