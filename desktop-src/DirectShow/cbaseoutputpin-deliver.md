---
description: Die Deliver-Methode übergibt ein Medien Beispiel an die verbundene Eingabe-PIN.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: Cbaseoutputpin. Deliver-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adc603e4cdd1f49e649264d2d82d6df0fb12569
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366864"
---
# <a name="cbaseoutputpindeliver-method"></a>Cbaseoutputpin. Deliver-Methode

Die- `Deliver` Methode übermittelt ein Medien Beispiel an die verbundene Eingabe-PIN.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Deliver(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                           | Beschreibung                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ E \_ nicht \_ verbunden**</dt> </dl> | Die PIN ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode für die Eingabe-PIN auf. **Receive** kann blockieren, wenn die [**IMemInputPin:: receivecanblock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) -Methode S OK zurückgibt \_ .

Geben Sie das Beispiel nach dem Aufrufen dieser Methode frei. Die Eingabe-PIN kann einen Verweis Zähler für das Beispiel enthalten. verwenden Sie daher nicht das Beispiel. Rufen Sie immer die [**cbaseoutputpin:: getdeliverybuffer**](cbaseoutputpin-getdeliverybuffer.md) -Methode auf, um ein neues Beispiel zu erhalten.

Speichern Sie den kritischen Abschnitt des Filters, bevor Sie diese Methode aufrufen. Andernfalls wird die PIN während des Methoden Aufrufes möglicherweise getrennt. Wenn der Filter einen Arbeits Thread zum Übermitteln von Beispielen verwendet, halten Sie den kritischen Abschnitt gedrückt, wenn der Filter bereit ist, ein Beispiel zu liefern. Andernfalls können Sie den kritischen Abschnitt in der [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode des Filters speichern, in dem der Filter Beispiele verarbeitet.

Arbeitsthreads können zu einem möglichen Deadlock führen. Wenn der Thread den kritischen Abschnitt enthält, kann er auf eine Zustandsänderung im Filter warten. Gleichzeitig wartet die Zustandsänderung möglicherweise darauf, dass der Thread beendet wird. Um dies zu verhindern, sollte der Code für die Zustandsänderung ein Ereignis signalisieren, das den Thread beendet, und dann auf den Abschluss des Threads warten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseoutputpin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




