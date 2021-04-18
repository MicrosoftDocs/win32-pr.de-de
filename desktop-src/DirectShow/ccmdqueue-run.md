---
description: Die Run-Methode wechselt in den Modus "wird ausgeführt", sodass Befehle, die von der streamzeit verzögert werden, ausgeführt werden können.
ms.assetid: c529ae84-c9b7-46f1-a1e4-716fc9e9df13
title: Ccmdqueue. Run-Methode (winutil. h)
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
ms.openlocfilehash: 424914e53a12ff0f43e8b7e2a3345c28d84437d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365901"
---
# <a name="ccmdqueuerun-method"></a>Ccmdqueue. Run-Methode

Die `Run` Methode wechselt in den Modus "wird ausgeführt", sodass Befehle, die von der streamzeit verzögert werden, ausgeführt werden können.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Run(
   REFERENCE_TIME tStreamTimeOffset
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tstreamtimeoffset* 
</dt> <dd>

Offset Zeit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Während des laufenden Modus ist die Zuordnung von streamzeit zu Präsentationszeit bekannt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccmdqueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




