---
description: Die ThreadProc-Methode ist die Threadprozedur.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: WEBCAMThread.ThreadProc-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6419d315e162f859f49ee2448758999ca194adf8c16c6210f77d919fa2a18f47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662110"
---
# <a name="camthreadthreadproc-method"></a>CAMThread.ThreadProc-Methode

Die `ThreadProc` -Methode ist die Threadprozedur.

## <a name="syntax"></a>Syntax


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD-Wert** zurück, dessen Bedeutung von der abgeleiteten Klasse definiert wird.

## <a name="remarks"></a>Hinweise

Dies ist eine rein virtuelle Methode. Implementieren Sie diese Methode in der abgeleiteten Klasse, um eine Threadprozedur zu erstellen. Wenn die [**METHODECAMThread::Create**](camthread-create.md) einen Thread erstellt, gibt sie die Adresse [**derCAMThread::InitialThreadProc-Methode**](camthread-initialthreadproc.md) an, die wiederum Ihre ThreadProc-Methode aufruft.

In der Regel gibt Ihre ThreadProc-Methode eine Schleife ein, die Anforderungen abruft (durch Aufrufen der [**METHODENCAMThread::GetRequest**](camthread-getrequest.md) [**oderCAMThread::CheckRequest)**](camthread-checkrequest.md) und Daten verarbeitet.

Wenn diese Methode zurückgegeben wird, wird der Thread beendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




