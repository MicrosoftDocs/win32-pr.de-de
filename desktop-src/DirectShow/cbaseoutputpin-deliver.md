---
description: Die Deliver-Methode liefert ein Medienbeispiel an den verbundenen Eingabepin.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: CBaseOutputPin.Deliver-Methode (Amfilter.h)
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
ms.openlocfilehash: f6786e9e763af26619b2dc4f6abc25aa2fd9527d7278e7da02f6042908e56bdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341380"
---
# <a name="cbaseoutputpindeliver-method"></a>CBaseOutputPin.Deliver-Methode

Die `Deliver` -Methode übergibt ein Medienbeispiel an den verbundenen Eingabepin.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT Deliver(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle des**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                           | Beschreibung                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>              |
| <dl> <dt>**VFW \_ E \_ NICHT \_ VERBUNDEN**</dt> </dl> | Die Stecknadel ist nicht verbunden.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die [**IMemInputPin::Receive-Methode für**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) den Eingabepin auf. **Receive** kann blockieren, wenn die [**IMemInputPin::ReceiveCanBlock-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) S \_ OK zurückgibt.

Geben Sie das Beispiel nach dem Aufruf dieser Methode frei. Der Eingabepin kann einen Verweiszähler für das Beispiel speichern, daher sollten Sie das Beispiel nicht wiederverwenden. Rufen Sie immer die [**CBaseOutputPin::GetDeliveryBuffer-Methode**](cbaseoutputpin-getdeliverybuffer.md) auf, um ein neues Beispiel zu erhalten.

Halten Sie den kritischen Abschnitt des Filters, bevor Sie diese Methode aufrufen. Andernfalls wird die Verbindung mit dem Pin während des Methodenaufrufs möglicherweise getrennt. Wenn der Filter einen Arbeitsthread verwendet, um Beispiele zu liefern, halten Sie den kritischen Abschnitt, wenn der Filter bereit ist, ein Beispiel zu liefern. Andernfalls können Sie den kritischen Abschnitt in der [**IMemInputPin::Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) des Filters halten, in der der Filter Stichproben verarbeitet.

Arbeitsthreads können einen potenziellen Deadlock erzeugen. Wenn der Thread den kritischen Abschnitt enthält, kann er auf eine Zustandsänderung im Filter warten. Gleichzeitig kann die Zustandsänderung auf den Abschluss des Threads warten. Um dies zu verhindern, sollte der Code zur Zustandsänderung ein Ereignis signalisieren, das den Thread beendet, und dann warten, bis der Thread den Abschluss signalisiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseOutputPin-Klasse**](cbaseoutputpin.md)
</dt> </dl>

 

 




