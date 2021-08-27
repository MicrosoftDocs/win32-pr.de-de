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
ms.openlocfilehash: e042624573cd0c421e8ecd202cde971a49eef95cc5f3c6c0ac64bf45b4cf9c19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103330"
---
# <a name="camthreadcamthread-constructor"></a>CABThread.MSIThread-Konstruktor

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

Aus Gründen der Abwärtskompatibilität mit früheren Versionen von strmbase.lib wird für diesen Parameter standardmäßig **NULL** verwendet. Die Übergabe eines Werts ungleich **NULL** wird jedoch bevorzugt, damit der Aufrufer den Status des Objekts überprüfen kann.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Konstruktormethode erstellt den Thread nicht. Um den Thread zu erstellen, rufen Sie die [**METHODE TARThread::Create**](camthread-create.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WEBCAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




