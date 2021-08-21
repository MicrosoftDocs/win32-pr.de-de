---
description: Die Close-Methode wartet darauf, dass der Thread beendet wird, und gibt dann seine Ressourcen frei.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: CAMThread.Close-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf12a80cd967832755f476db0e8810867326e84598ddce835e1da10dc6943419
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158931"
---
# <a name="camthreadclose-method"></a>CAMThread.Close-Methode

Die `Close` -Methode wartet darauf, dass der Thread beendet wird, und gibt dann seine Ressourcen frei.

## <a name="syntax"></a>Syntax


```C++
void Close();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Bevor Sie diese Methode aufrufen, müssen Sie eine Möglichkeit zum Beenden des Threads bereitstellen. Definieren Sie z. B. in Ihrer [**METHODE "CAMThread::ThreadProc"**](camthread-threadproc.md) eine Anforderung, die das Beenden des Threads signalisiert. Rufen Sie dann die [**METHODECAMThread::CallWorker mit**](camthread-callworker.md) diesem Wert auf.

Die [**~CAMThread-Destruktormethode**](camthread--camthread.md) ruft diese Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




