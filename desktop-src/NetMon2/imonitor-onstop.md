---
description: Die OnStop-Methode muss vom Monitor implementiert werden. MSCVC ruft diese Methode auf, um den Monitor zu benachrichtigen, dass die Erfassung beendet wird.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: IMonitor::OnStop-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStop
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: cb81042395de2a2381921cfd0b30c18af22df320b8ce8db228cf65743b1fe334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778990"
---
# <a name="imonitoronstop-method"></a>IMonitor::OnStop-Methode

Die **OnStop-Methode** muss vom Monitor implementiert werden. MSCVC ruft diese Methode auf, um den Monitor zu benachrichtigen, dass die Erfassung beendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnStop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert S OK (was mit \_ NOERROR identisch ist).

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode. Wenn ein Fehlercode zurückgegeben wird, kann der Monitor nicht neu gestartet werden.

## <a name="remarks"></a>Hinweise

McSVC ruft diese Methode auf, nachdem [IRTC::Stop](irtc-stop.md) aufgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




