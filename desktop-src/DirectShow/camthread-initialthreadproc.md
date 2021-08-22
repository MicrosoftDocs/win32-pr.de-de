---
description: Die InitialThreadProc-Methode ruft die Hauptthreadprozedur auf.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.InitialThreadProc-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d12e8d41ac0c6e1fd2af06c21accbb5c62e4eb25f2fc3f6c36988101a9b64d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540300"
---
# <a name="camthreadinitialthreadproc-method"></a>CAMThread.InitialThreadProc-Methode

Die `InitialThreadProc` -Methode ruft die Hauptthreadprozedur auf.

## <a name="syntax"></a>Syntax


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pv* 
</dt> <dd>

`this` Zeiger.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das von [**CABThread::ThreadProc**](camthread-threadproc.md)zurückgegebene **DWORD** zurück. Die abgeleitete Klasse definiert diesen Wert.

## <a name="remarks"></a>Hinweise

Die [**METHODE TARThread::Create**](camthread-create.md) verwendet diese Methode für die Threadprozedur, wenn der Thread erstellt wird. Er verwendet den `this` Zeiger als Threadargument.

Diese Methode ruft die [**METHODE FLYThread::CoInitializeHelper**](camthread-coinitializehelper.md) und dann ThreadProc auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WEBCAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




