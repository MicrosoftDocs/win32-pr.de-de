---
description: Konstruktormethode.
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Cammsgevent. cammsgevent-Konstruktor (wxutil. h)
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
ms.openlocfilehash: 0d207afae53a715728d8307656b0c2427ce9574c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358763"
---
# <a name="cammsgeventcammsgevent-constructor"></a>Cammsgevent. cammsgevent-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Wert. Wenn der Konstruktor ausfällt, empfängt dieser Parameter einen Fehlercode. Wenn dies auftritt, befindet sich das Objekt nicht in einem gültigen Zustand.

Aus Gründen der Abwärtskompatibilität mit früheren Versionen von "straumbase. lib" ist dieser Parameter standardmäßig **null**. Die Übergabe eines Werts ungleich **null** wird jedoch bevorzugt, sodass der Aufrufer den Status des Objekts überprüfen kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cammsgevent-Klasse**](cammsgevent.md)
</dt> </dl>

 

 




