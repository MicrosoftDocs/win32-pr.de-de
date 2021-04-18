---
description: Die checktime-Methode bestimmt, ob eine angegebene Zeit fällig ist.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Ccmdqueue. checktime-Methode (winutil. h)
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
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372753"
---
# <a name="ccmdqueuechecktime-method"></a>Ccmdqueue. checktime-Methode

Die- `CheckTime` Methode bestimmt, ob eine angegebene Zeit fällig ist.

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

Zeit bis zur Überprüfung.

</dd> <dt>

*bStream* 
</dt> <dd>

**True** , wenn der *Zeit* Parameter ein streamzeitwert ist. **False** , wenn *time* ein Präsentationszeit Wert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die angegebene Zeit noch nicht überschritten wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccmdqueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




