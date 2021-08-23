---
description: Die CheckTime-Methode bestimmt, ob eine angegebene Zeit fällig ist.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: CCmdQueue.CheckTime-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 826b59d12c135e9c86ce923f37e1558dca4f13efafb4880aecab1384829a484a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910430"
---
# <a name="ccmdqueuechecktime-method"></a>CCmdQueue.CheckTime-Methode

Die `CheckTime` -Methode bestimmt, ob eine angegebene Zeit fällig ist.

## <a name="syntax"></a>Syntax


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*time* 
</dt> <dd>

Zeit, die überprüft werden soll.

</dd> <dt>

*bStream* 
</dt> <dd>

**TRUE,** wenn der *Time-Parameter* ein Streamzeitwert ist; **FALSE,** wenn *time* ein Präsentationszeitwert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn die angegebene Zeit noch nicht überschritten wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CCmdQueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




