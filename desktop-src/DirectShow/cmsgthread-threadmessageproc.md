---
description: Verarbeitet Anforderungen. Dies ist eine reine virtuelle Memberfunktion.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: CMsgThread.ThreadMessageProc-Methode (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ThreadMessageProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb11a7cac567bd645d0e3fd1c294636b5df9410fbc54012633ec0c0d161b43d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909700"
---
# <a name="cmsgthreadthreadmessageproc-method"></a>CMsgThread.ThreadMessageProc-Methode

Verarbeitet Anforderungen. Dies ist eine reine virtuelle Memberfunktion.

## <a name="syntax"></a>Syntax


```C++
virtual LRESULT ThreadMessageProc(
   UINT     uMsg,
   DWORD    dwFlags,
   LPVOID   lpParam,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uMsg* 
</dt> <dd>

Anforderungscode.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Optionaler flag-Parameter, der angefordert werden soll.

</dd> <dt>

*lpParam* 
</dt> <dd>

Optionaler Zeiger auf zusätzliche Daten oder einen Rückgabedatenblock.

</dd> <dt>

*pEvent* 
</dt> <dd>

Optionaler Zeiger auf ein Ereignisobjekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Jede Rückgabe ungleich 0 führt dazu, dass der Thread beendet wird. Gibt 0 (null) zurück, es sei denn, eine Beendigungsanforderung wurde kürzlich verarbeitet.

## <a name="remarks"></a>Hinweise

Diese rein virtuelle Funktion muss in Ihrer abgeleiteten Klasse überschrieben werden. Sie wird einmal für jede Anforderung aufgerufen, die durch einen Aufruf der [**Memberfunktion CMsgThread::P utThreadMsg**](cmsgthread-putthreadmsg.md) in die Warteschlange eingereiht wird.

Die Memberfunktion definiert die vier Parameter. Verwenden Sie in der Regel den *uMsg-Parameter,* um die Anforderung anzugeben, und die anderen drei Parameter sind optionale zusätzliche Parameter. Die aufrufende Anwendung kann einen Zeiger auf ein [**TAREvent-Objekt**](camevent.md) im *pEvent-Parameter* bereitstellen, wenn dies für Ihre Anwendung erforderlich ist. Sie müssen dieses Ereignis nach der Verarbeitung des Ereignisses mithilfe eines Ausdrucks festlegen, z. B.:


```C++
pEvent->SetEvent
```



Ein Anforderungscode muss zurückgestellt werden, um den Arbeitsthread anzuweisen, den Code zu beenden. Geben Sie nach Dem Empfang dieser Anforderung 1 von dieser Memberfunktion zurück. Gibt 0 zurück, wenn der Arbeitsthread nicht beendet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMsgThread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




