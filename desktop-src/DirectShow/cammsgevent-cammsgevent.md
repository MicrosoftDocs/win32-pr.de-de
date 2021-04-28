---
description: 'OEMMsgEvent.OEMMsgEvent-Konstruktor : Konstruktormethode.'
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: OEMMsgEvent.OEMMsgEvent-Konstruktor (Wxutil.h)
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
ms.openlocfilehash: dac72ecb97a1ea1fd2594af9c11b8a03078cf2cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096534"
---
# <a name="cammsgeventcammsgevent-constructor"></a>OEMMsgEvent.OEMMsgEvent-Konstruktor

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

Aus Gründen der Abwärtskompatibilität mit früheren Versionen von strmbase.lib wird dieser Parameter standardmäßig auf **NULL festgelegt.** Die Übergabe eines Werts, der nicht **NULL** ist, wird jedoch bevorzugt, damit der Aufrufer den Status des Objekts überprüfen kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (streams.h enthalten)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CAMMsgEvent-Klasse**](cammsgevent.md)
</dt> </dl>

 

 




