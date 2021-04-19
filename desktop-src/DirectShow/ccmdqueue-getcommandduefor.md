---
description: Die getcommandduefor-Methode ruft einen verzögerten Befehl ab, der zu einem bestimmten Zeitpunkt geplant wird.
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: Ccmdqueue. getcommandduefor-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48a01436a68a5b98d08880c1516bbf4576d10be2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350770"
---
# <a name="ccmdqueuegetcommandduefor-method"></a>Ccmdqueue. getcommandduefor-Methode

Die- `GetCommandDueFor` Methode ruft einen verzögerten Befehl ab, der zu einem bestimmten Zeitpunkt geplant wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tstream* 
</dt> <dd>

Der Zeitpunkt, zu dem der Befehl geplant ist.

</dd> <dt>

*ppCmd* 
</dt> <dd>

Adresse eines Zeigers auf den verzögerten Befehl, der zu dem im *tstream* -Parameter angegebenen Zeitpunkt ausgeführt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt VFW \_ E \_ nicht \_ gefunden zurück, wenn keine Befehle fällig sind; andernfalls gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion nimmt eine streamzeit an und gibt den verzögerten Befehl zurück, der zu diesem Zeitpunkt geplant ist. Der tatsächliche Offset der streamzeit wird berechnet, wenn die Befehls Warteschlange ausgeführt wird. Befehle bleiben bis zum Ausführen oder Abbrechen in die Warteschlange eingereiht. Diese Member-Funktion wird nicht blockiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccmdqueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




