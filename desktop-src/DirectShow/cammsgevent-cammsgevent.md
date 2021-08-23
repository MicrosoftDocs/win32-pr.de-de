---
description: CABMsgEvent.CABMsgEvent-Konstruktor – Konstruktormethode.
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: CABMsgEvent.CABMsgEvent-Konstruktor (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fc2eeaab10134022388e6a57628d1c3c5a87fc0e0a443efab19f016a1e5c27b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955499"
---
# <a name="cammsgeventcammsgevent-constructor"></a>CABMsgEvent.CABMsgEvent-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Wenn der Konstruktor fehlschlägt, empfängt dieser Parameter einen Fehlercode. In diesem Fall befindet sich das Objekt nicht in einem gültigen Zustand.

Aus Gründen der Abwärtskompatibilität mit früheren Versionen von strmbase.lib wird für diesen Parameter standardmäßig **NULL** verwendet. Die Übergabe eines Werts ungleich **NULL** wird jedoch bevorzugt, damit der Aufrufer den Status des Objekts überprüfen kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WEBCAMMsgEvent-Klasse**](cammsgevent.md)
</dt> </dl>

 

 




