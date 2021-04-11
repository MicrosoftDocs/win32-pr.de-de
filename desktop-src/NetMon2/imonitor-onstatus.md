---
description: Die mcsvc-Methode ruft die OnStatus-Methode auf, um den Monitor zu benachrichtigen, dass ein NPP-Status Ereignis vorhanden ist. Diese Methode muss vom Monitor implementiert werden.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'Imonitor:: OnStatus-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130261"
---
# <a name="imonitoronstatus-method"></a>Imonitor:: OnStatus-Methode

Die mcsvc-Methode ruft die **OnStatus** -Methode auf, um den Monitor zu benachrichtigen, dass ein NPP-Status Ereignis vorhanden ist. Diese Methode muss vom Monitor implementiert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ereignis* \[ in\]
</dt> <dd>

Eine [Update- \_ Ereignis](update-event.md) Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK (entspricht noError), und der mcsvc übergibt den zurückgegebenen Wert zur Verarbeitung an den NPP zurück.

Wenn die Methode nicht erfolgreich ist, wird ein Fehlercode zurückgegeben. Bei einem Fehler übergibt der mcsvc den zurückgegebenen Wert zur Verarbeitung an den NPP zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




