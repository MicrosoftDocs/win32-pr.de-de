---
description: Die asynchronousblockoutputpin-Methode blockiert die PIN. Die-Methode gibt möglicherweise zurück, bevor die PIN blockiert wird.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Cdynamicoutputpin. asynchronousblockoutputpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67232bf1081f9c9ea088968cb6c5d02667b00eeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358145"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a>Cdynamicoutputpin. asynchronousblockoutputpin-Methode

Die- `AsynchronousBlockOutputPin` Methode blockiert die PIN. Die-Methode gibt möglicherweise zurück, bevor die PIN blockiert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hnotifycallerpinblockedevent* 
</dt> <dd>

Handle für ein Ereignis. Das-Ereignis wird signalisiert, wenn die Ausgabepin blockiert ist, oder, wenn der Aufrufer den Block Vorgang abbricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                                                                    | Beschreibung                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Erfolg.<br/>                                      |
| <dl> <dt>**VFW \_ E \_ Pin \_ bereits \_ blockiert**</dt> </dl>                   | Die PIN ist bereits in einem anderen Thread blockiert.<br/>     |
| <dl> <dt>**VFW \_ E \_ Pin \_ ist \_ \_ in \_ diesem \_ Thread bereits blockiert.**</dt> </dl> | Die PIN ist bereits im aufrufenden Thread blockiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode nicht aus dem streamingthread aufzurufen.

Wenn kein streamingingthread die PIN verwendet, blockiert diese Methode sofort die PIN. Andernfalls wird der PIN-Status auf "Pending" festgelegt, und es wird zurückgegeben. Wenn der Streamingvorgang abgeschlossen ist, ruft der streamingthread die [**cdynamicoutputpin:: stopusingoutputpin**](cdynamicoutputpin-stopusingoutputpin.md) -Methode auf, die die PIN blockiert und das **hnotifycallerpinblockedevent** -Ereignis signalisiert. Um einen ausstehenden Block abzubrechen, rufen Sie die [**cdynamicoutputpin:: unblockoutputpin**](cdynamicoutputpin-unblockoutputpin.md) -Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




