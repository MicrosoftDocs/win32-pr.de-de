---
description: Die Cancel-Methode bricht eine zuvor in die Warteschlange eingereihte CDeferredCommand::Invoke-Anforderung ab.
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: CDeferredCommand.Cancel-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa7e957fe97e06c6fb14fe3a9048048e351ac1baf4ff8f4dae25b3cf5863776e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043710"
---
# <a name="cdeferredcommandcancel-method"></a>CDeferredCommand.Cancel-Methode

Die `Cancel` -Methode bricht eine zuvor in die Warteschlange [**eingereihte CDeferredCommand::Invoke-Anforderung**](cdeferredcommand-invoke.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt VFW \_ E \_ ALREADY \_ CANCELLED zurück, wenn **m \_ pQueue** **NULL** ist. Gibt ein **HRESULT** aus [**CCmdQueue::Remove zurück,**](ccmdqueue-remove.md) wenn der Aufruf einen Fehler generiert. Gibt bei Erfolg S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IDeferredCommand::Cancel-Methode.**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDeferredCommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




