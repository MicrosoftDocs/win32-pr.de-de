---
description: Die Close-Methode wartet darauf, dass der Thread beendet wird, und gibt dann seine Ressourcen frei.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Camthread. Close-Methode (wxutil. h)
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
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362051"
---
# <a name="camthreadclose-method"></a>Camthread. Close-Methode

Die- `Close` Methode wartet, bis der Thread beendet wird, und gibt dann die zugehörigen Ressourcen frei.

## <a name="syntax"></a>Syntax


```C++
void Close();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Vor dem Aufrufen dieser Methode müssen Sie eine Möglichkeit zum Beenden des Threads bereitstellen. Definieren Sie beispielsweise in der Methode " [**camthread:: ThreadProc**](camthread-threadproc.md) " eine Anforderung, mit der der Thread beendet wird. Rufen Sie dann die Methode " [**camthread:: callworker**](camthread-callworker.md) " mit diesem Wert auf.

Die [**~ camthread**](camthread--camthread.md) -deeinigermethode ruft diese Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




