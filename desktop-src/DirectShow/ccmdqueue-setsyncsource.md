---
description: Mit der setsyncsource-Methode wird die Uhrzeit für die zeitliche Steuerung festgelegt.
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: Ccmdqueue. setsyncsource-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 995df3afa5185d8f50278899ac6a5d67dc6d230e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370499"
---
# <a name="ccmdqueuesetsyncsource-method"></a>Ccmdqueue. setsyncsource-Methode

Die- `SetSyncSource` Methode legt die Zeit für die zeitliche Steuerung fest.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT SetSyncSource(
   IReferenceClock *pIrc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pirc* 
</dt> <dd>

Zeiger auf die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccmdqueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




