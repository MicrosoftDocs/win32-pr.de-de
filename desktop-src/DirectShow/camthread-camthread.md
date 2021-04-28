---
description: 'CABThread.WEBCAMThread-Konstruktor : Konstruktormethode.'
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: CABThread.MSIThread-Konstruktor (Wxutil.h)
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
ms.openlocfilehash: 0c4b9c5f80e131ce089b6a2da924e9cca41a84f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096408"
---
# <a name="camthreadcamthread-constructor"></a>CABThread.CABThread-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Wenn der Konstruktor fehlschlägt, empfängt dieser Parameter einen Fehlercode. In diesem Fall befindet sich das Objekt nicht in einem gültigen Zustand.

Aus Gründen der Abwärtskompatibilität mit früheren Versionen von strmbase.lib wird dieser Parameter standardmäßig auf **NULL** gesetzt. Die Übergabe eines Werts ungleich **NULL** wird jedoch bevorzugt, damit der Aufrufer den Status des Objekts überprüfen kann.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Konstruktormethode erstellt den Thread nicht. Um den Thread zu erstellen, rufen Sie die [**METHODE TARThread::Create**](camthread-create.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WEBCAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




