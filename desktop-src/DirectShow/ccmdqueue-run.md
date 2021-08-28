---
description: Die Run-Methode wechselt in den Ausführungsmodus, sodass Befehle, die um die Streamzeit zurückgestellt werden, ausgeführt werden können.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: CCmdQueue.Run-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5da70c4ac0c5890e4483f7facdc4d1f5a3d5dd70906c53917bd83029dfaa6c6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757140"
---
# <a name="ccmdqueuerun-method"></a>CCmdQueue.Run-Methode

Die `Run` -Methode wechselt in den Ausführungsmodus, sodass Befehle, die durch die Streamzeit zurückgestellt werden, ausgeführt werden können.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tStreamTimeOffset* 
</dt> <dd>

Offsetzeit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Während des Ausführungsmodus ist die Zuordnung von Streamzeit zu Präsentationszeit bekannt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CCmdQueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




