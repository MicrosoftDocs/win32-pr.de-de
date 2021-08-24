---
description: Die CheckRequest-Methode überprüft, ob eine Threadanforderung ohne Blockierung vor liegt.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: CSourceStream.CheckRequest-Methode (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bb77358ec579415439c2832b00255e7ffeb3c7eba0e387bfa0522a4a5109669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073314"
---
# <a name="csourcestreamcheckrequest-method"></a>CSourceStream.CheckRequest-Methode

Die `CheckRequest` -Methode überprüft, ob eine Threadanforderung ohne Blockierung vor liegt.

## <a name="syntax"></a>Syntax


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCom* 
</dt> <dd>

Zeiger auf eine Variable, die den Wert empfängt, der beim letzten Aufruf [**derCAMThread::CallWorker-Methode übergeben**](camthread-callworker.md) wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn eine ausstehende Anforderung vorsteht, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt [**dieCAMThread::CheckRequest-Methode,**](camthread-checkrequest.md) um die Typüberprüfung durchzuführen. Die **CSourceStream-Klasse** definiert den folgenden enumerierten Typ für den *pCom-Parameter:*


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSourceStream-Klasse**](csourcestream.md)
</dt> </dl>

 

 




