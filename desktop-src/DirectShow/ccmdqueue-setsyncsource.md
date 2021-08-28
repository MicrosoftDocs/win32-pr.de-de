---
description: Die SetSyncSource-Methode legt die für die Zeitsteuerung verwendete Uhr fest.
ms.assetid: 646d4d24-f9b7-438a-b842-58e90eb6a945
title: CCmdQueue.SetSyncSource-Methode (Winutil.h)
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
ms.openlocfilehash: 3877fb52a1e2268d24974ee3575c712d27a107f4429398ada9de1ebf5e728675
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757150"
---
# <a name="ccmdqueuesetsyncsource-method"></a>CCmdQueue.SetSyncSource-Methode

Die `SetSyncSource` -Methode legt die für die Zeitsteuerung verwendete Uhr fest.

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

Zeiger auf die [**IReferenceClock-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CCmdQueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




