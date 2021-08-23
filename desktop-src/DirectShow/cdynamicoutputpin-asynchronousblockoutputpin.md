---
description: Die AsynchronousBlockOutputPin-Methode blockiert die Stecknadel. Die -Methode gibt möglicherweise zurück, bevor die Stecknadel blockiert wird.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: CDynamicOutputPin.AsynchronousBlockOutputPin-Methode (Amfilter.h)
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
ms.openlocfilehash: c8999f6dbb42c55c036ee3d7fcd02dc34def4bd0a036cf0b5d908d3c280e297e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317790"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a>CDynamicOutputPin.AsynchronousBlockOutputPin-Methode

Die `AsynchronousBlockOutputPin` -Methode blockiert die Stecknadel. Die -Methode gibt möglicherweise zurück, bevor die Stecknadel blockiert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hNotifyCallerPinBlockedEvent* 
</dt> <dd>

Handle für ein Ereignis. Das Ereignis wird signalisiert, wenn der Ausgabepin blockiert wird oder wenn der Aufrufer den Blockvorgang abbricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                                                                    | Beschreibung                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Erfolg.<br/>                                      |
| <dl> <dt>**VFW \_ \_ E-PIN \_ BEREITS \_ BLOCKIERT**</dt> </dl>                   | Das Anheften ist bereits in einem anderen Thread blockiert.<br/>     |
| <dl> <dt>**VFW \_ \_ E-PIN \_ FÜR \_ DIESEN \_ \_ \_ THREAD BEREITS BLOCKIERT**</dt> </dl> | Pin ist im aufrufenden Thread bereits blockiert.<br/> |



 

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode nicht aus dem Streamingthread auf.

Wenn kein Streamingthread den Stecknadel verwendet, blockiert diese Methode den Pin sofort. Andernfalls wird der Stecknadelstatus auf "Ausstehend" festgelegt und zurückgegeben. Nach Abschluss des Streamingvorgangs ruft der Streamingthread die [**CDynamicOutputPin::StopUsingOutputPin-Methode**](cdynamicoutputpin-stopusingoutputpin.md) auf, die den Pin blockiert und das **hNotifyCallerPinBlockedEvent-Ereignis** signalisiert. Um einen ausstehenden Block abzubrechen, rufen Sie die [**CDynamicOutputPin::UnblockOutputPin-Methode**](cdynamicoutputpin-unblockoutputpin.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




