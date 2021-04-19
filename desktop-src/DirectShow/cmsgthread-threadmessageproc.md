---
description: Verarbeitet Anforderungen. Dies ist eine reine virtuelle Member-Funktion.
ms.assetid: ffdbc287-ca17-44e4-b00a-d72a2367f510
title: Cmsgthread. threadmessageproc-Methode (msgthrd. h)
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
ms.openlocfilehash: cf47eb63a6f9d8fe4921985bb64567de6678b44c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368640"
---
# <a name="cmsgthreadthreadmessageproc-method"></a>Cmsgthread. threadmessageproc-Methode

Verarbeitet Anforderungen. Dies ist eine reine virtuelle Member-Funktion.

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

*Umschlag* 
</dt> <dd>

Anforderungs Code.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Optionaler Flag-Parameter für die Anforderung.

</dd> <dt>

*lpparam* 
</dt> <dd>

Optionaler Zeiger auf zusätzliche Daten oder einen Rückgabe Datenblock.

</dd> <dt>

*Peer Event* 
</dt> <dd>

Optionaler Zeiger auf ein Ereignis Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Rückgabe ungleich NULL bewirkt, dass der Thread beendet wird. Gibt NULL zurück, es sei denn, eine Beendigungs Anforderung wurde kürzlich verarbeitet.

## <a name="remarks"></a>Bemerkungen

Diese reine virtuelle Funktion muss in der abgeleiteten Klasse überschrieben werden. Sie wird einmal für jede Anforderung aufgerufen, die durch einen Aufruf der [**cmsgthread::P utthreadmsg**](cmsgthread-putthreadmsg.md) -Member-Funktion in der Warteschlange eingereiht wird.

Die Member-Funktion definiert die vier Parameter. Verwenden Sie in der Regel den Parameter " *übersg* ", um die Anforderung anzugeben, und die anderen drei Parameter sind optionale zusätzliche Parameter. Die aufrufenden Anwendung kann einen Zeiger auf ein [**camevent**](camevent.md) -Objekt im Parameter " *GVENT* " bereitstellen, wenn dies für Ihre Anwendung erforderlich ist. Sie müssen dieses Ereignis festlegen, nachdem Sie das Ereignis mithilfe eines Ausdrucks wie z. b. verarbeitet haben:


```C++
pEvent->SetEvent
```



Ein Anforderungs Code muss reserviert werden, um dem Arbeits Thread mitzuteilen, dass er beendet werden soll. Wenn diese Anforderung empfangen wird, wird 1 von dieser Member-Funktion zurückgegeben. Gibt 0 zurück, wenn der Arbeits Thread nicht beendet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmsgthread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




