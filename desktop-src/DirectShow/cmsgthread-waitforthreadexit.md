---
description: Blockiert, bis der Thread beendet wird.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: CMsgThread.WaitForThreadExit-Methode (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de9861a1c7cae3055be288c4624b9e0b98c7b719e1534c1841ddb17770d91cf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915710"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a>CMsgThread.WaitForThreadExit-Methode

Blockiert, bis der Thread beendet wird.

## <a name="syntax"></a>Syntax


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpdwExitCode* 
</dt> <dd>

Zeiger auf den vom Thread zurückgegebenen Exitcode.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt entweder **TRUE** oder **FALSE** zurück, deren Bedeutung von der Klasse bestimmt wird, die die überschriebene [**CMsgThread::ThreadMessageProc-Memberfunktion**](cmsgthread-threadmessageproc.md) und die aufrufende Memberfunktion angibt.

## <a name="remarks"></a>Hinweise

Stellen Sie sicher, dass der Arbeitsthread vollständig beendet wurde, bevor Sie die Zerstörung Ihrer abgeleiteten Klasse abschließen. Andernfalls wird der Thread möglicherweise weiterhin ausgeführt, nachdem Die Dynamic Link Library (DLL) aus dem Adressraum des Prozesses entladen wurde. Selbst wenn die einzige anweisung, die beendet werden muss, eine einzelne Rückgabeanweisung ist, würde dies eine Ausnahme verursachen. Die einzige zuverlässige Möglichkeit, sicherzustellen, dass der Thread beendet wurde, besteht darin, dem Thread das Beenden zu signalisieren (mithilfe eines privat ausgehandelten [**CMsg-Objekts,**](cmsg.md) das an die [**Memberfunktion CMsgThread::P utThreadMsg**](cmsgthread-putthreadmsg.md) gesendet wird) und dann diese Memberfunktion aufzurufen. Dies sollten Sie im Destruktor für Ihre abgeleitete Klasse tun.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMsgThread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




