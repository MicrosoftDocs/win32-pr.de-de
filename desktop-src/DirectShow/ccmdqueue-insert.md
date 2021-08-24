---
description: Die Insert-Methode fügt der Warteschlange ein CDeferredCommand-Objekt hinzu.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: CCmdQueue.Insert-Methode (Winutil.h)
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
ms.openlocfilehash: 90e2bab4a3545e8a02315155ad4a477511ecf961c93a511ccba268b7fde7dd0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757320"
---
# <a name="ccmdqueueinsert-method"></a>CCmdQueue.Insert-Methode

Die `Insert` -Methode fügt der Warteschlange ein [**CDeferredCommand-Objekt**](cdeferredcommand.md) hinzu.

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

Zeiger auf das **CDeferredCommand-Objekt,** das der Warteschlange hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK in der Standardimplementierungen zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CCmdQueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




