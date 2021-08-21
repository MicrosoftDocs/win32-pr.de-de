---
description: Die EOS-Methode übergibt einen End-of-Stream-Aufruf an den Eingabepin.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: COutputQueue.EOS-Methode (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3effb06498ae65cad8eefd9a3144cab140926006cd38acee45c553c4295b0a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537140"
---
# <a name="coutputqueueeos-method"></a>COutputQueue.EOS-Methode

Die `EOS` -Methode übergibt einen End-of-Stream-Aufruf an den Eingabepin.

## <a name="syntax"></a>Syntax


```C++
void EOS();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn das Objekt einen Thread verwendet, wird eine MESSAGE-Steuerungsmeldung des Paketpakets \_ in die Warteschlange gestellt. Der Thread stellt alle ausstehenden Beispiele zur Verfügung und ruft die [**IPin::EndOfStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) auf dem Eingabepin auf.

Wenn das Objekt keinen Thread verwendet, ruft es die [**COutputQueue::SendAnyway-Methode**](coutputqueue-sendanyway.md) auf, um ausstehende Stichproben zu übermitteln. Anschließend ruft sie **IPin::EndOfStream auf** dem Eingabepin auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




