---
description: Die onstoppt-Methode muss vom Monitor implementiert werden. Mscvc ruft diese Methode auf, um den Monitor zu benachrichtigen, dass die Erfassung beendet wird.
ms.assetid: 5988bfb8-2068-42a1-a774-6f6be9828568
title: 'Imonitor:: onstoppt-Methode (Netmon. h)'
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
ms.openlocfilehash: a737aa5bede443b63f2074239eec17ea8a205cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343038"
---
# <a name="imonitoronstop-method"></a>Imonitor:: onstoppt-Methode

Die **onstoppt** -Methode muss vom Monitor implementiert werden. Mscvc ruft diese Methode auf, um den Monitor zu benachrichtigen, dass die Erfassung beendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnStop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht noError).

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode. Wenn ein Fehlercode zurückgegeben wird, kann der Monitor nicht neu gestartet werden.

## <a name="remarks"></a>Bemerkungen

Die mcsvc ruft diese Methode auf, nachdem " [iritc:: Beendigung](irtc-stop.md) " aufgerufen wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




