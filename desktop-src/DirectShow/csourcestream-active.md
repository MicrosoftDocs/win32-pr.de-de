---
description: 'Die aktive Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist. Diese Methode überschreibt die cbasepin:: Active-Methode. Wenn die PIN verbunden ist, startet diese Methode den streamingingthread.'
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: Csourcestream. Active-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a161c82621f29b916e03fbc2e59ec762871940b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372432"
---
# <a name="csourcestreamactive-method"></a>Csourcestream. Active-Methode

Die- `Active` Methode benachrichtigt die PIN, dass der Filter jetzt aktiv ist. Diese Methode überschreibt die [**cbasepin:: Active**](cbasepin-active.md) -Methode. Wenn die PIN verbunden ist, startet diese Methode den streamingingthread.

## <a name="syntax"></a>Syntax


```C++
HRESULT Active();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                             | Beschreibung                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Die PIN ist bereits aktiv.<br/>  |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                    |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>  | Der Thread konnte nicht gestartet werden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csourcestream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




