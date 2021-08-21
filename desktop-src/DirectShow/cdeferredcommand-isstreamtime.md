---
description: Die IsStreamTime-Methode gibt an, ob der Befehl zur Streamzeit oder zur Präsentationszeit ausgeführt werden soll.
ms.assetid: 4fb315a4-1bc6-49c8-a47f-0a8a46f3f790
title: CDeferredCommand.IsStreamTime-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.IsStreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82c541220a2b89ecdd23e4676175f4c7b2aacd93aac008546349b38e7bc2455a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657203"
---
# <a name="cdeferredcommandisstreamtime-method"></a>CDeferredCommand.IsStreamTime-Methode

Die `IsStreamTime` -Methode gibt an, ob der Befehl zur Streamzeit oder zur Präsentationszeit ausgeführt werden soll.

## <a name="syntax"></a>Syntax


```C++
BOOL IsStreamTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn die Datenstromzeit festgelegt ist. andernfalls gibt **FALSE** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDeferredCommand-Klasse**](cdeferredcommand.md)
</dt> </dl>

 

 




