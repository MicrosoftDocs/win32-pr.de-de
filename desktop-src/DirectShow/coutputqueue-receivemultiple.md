---
description: Die receivemultiple-Methode übermittelt einen Batch mit Medien Beispielen an die Eingabe-PIN.
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: Coutputqueue. receivemultiple-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360286"
---
# <a name="coutputqueuereceivemultiple-method"></a>Coutputqueue. receivemultiple-Methode

Die- `ReceiveMultiple` Methode übermittelt einen Batch von Medien Beispielen an die Eingabe-PIN.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppsamples* 
</dt> <dd>

Adresse eines Zeigers auf ein Array von Beispielen.

</dd> <dt>

*nsamples* 
</dt> <dd>

Anzahl der Stichproben im Array.

</dd> <dt>

*nsamplesprocgelassene* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der erfolgreich übermittelten Stichproben empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                             | Beschreibung                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | End-of-Stream-Benachrichtigung empfangen, bevor dieses Beispiel verarbeitet wird.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                                           |



 

## <a name="remarks"></a>Bemerkungen

Wenn das Objekt einen Thread verwendet, fügt diese Methode alle im Array bestandenen Beispiele in die Warteschlange ein. Andernfalls ruft die-Methode die [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) -Methode für die Eingabe-PIN auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




