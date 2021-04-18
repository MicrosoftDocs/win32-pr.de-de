---
description: Konstruktormethode.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Camthread. camthread-Konstruktor (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abaac0c3b0330cd41db7ecd21f894733de10a1b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372235"
---
# <a name="camthreadcamthread-constructor"></a>Camthread. camthread-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Wert. Wenn der Konstruktor ausfällt, empfängt dieser Parameter einen Fehlercode. Wenn dies auftritt, befindet sich das Objekt nicht in einem gültigen Zustand.

Aus Gründen der Abwärtskompatibilität mit früheren Versionen von "straumbase. lib" ist dieser Parameter standardmäßig **null**. Die Übergabe eines Werts ungleich **null** wird jedoch bevorzugt, sodass der Aufrufer den Status des Objekts überprüfen kann.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Konstruktormethode erstellt nicht den Thread. Um den Thread zu erstellen, rufen Sie die Methode " [**camthread:: Create**](camthread-create.md) " auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




