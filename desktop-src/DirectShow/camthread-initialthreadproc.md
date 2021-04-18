---
description: Die initialthread proc-Methode ruft die Hauptthread Prozedur auf.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Initialthread proc-Methode (wxutil. h)
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
ms.openlocfilehash: cd7fd0aa12d0659776db7e39fb223095762fc209
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360936"
---
# <a name="camthreadinitialthreadproc-method"></a>CAMThread.Initialthread proc-Methode

Die- `InitialThreadProc` Methode ruft die Hauptthread Prozedur auf.

## <a name="syntax"></a>Syntax


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*teuren* 
</dt> <dd>

`this` Zeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das von " [**camthread:: ThreadProc**](camthread-threadproc.md)" zurückgegebene **DWORD** zurück. Diese Werte werden von der abgeleiteten Klasse definiert.

## <a name="remarks"></a>Bemerkungen

Die Methode " [**camthread:: Create**](camthread-create.md) " verwendet diese Methode für die Thread Prozedur, wenn der Thread erstellt wird. Der Zeiger wird `this` als Thread Argument verwendet.

Diese Methode ruft die Methode [**camthread:: coinitializehelper**](camthread-coinitializehelper.md) und dann ThreadProc auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




