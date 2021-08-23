---
description: Die MCSVC-Methode ruft die OnStatus-Methode auf, um den Monitor zu benachrichtigen, dass ein NPP-Statusereignis vorhanden ist. Diese Methode muss vom Monitor implementiert werden.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: IMonitor::OnStatus-Methode (Netmon.h)
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
ms.openlocfilehash: 2a82594400bebc8a529290e0e0e881603172aa45c111d2d4d83ebcbd5ebfbeb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779040"
---
# <a name="imonitoronstatus-method"></a>IMonitor::OnStatus-Methode

Die MCSVC-Methode ruft die **OnStatus-Methode** auf, um den Monitor zu benachrichtigen, dass ein NPP-Statusereignis vorhanden ist. Diese Methode muss vom Monitor implementiert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ereignis* \[ In\]
</dt> <dd>

Eine [UPDATE \_ EVENT-Struktur.](update-event.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert S OK (was mit NOERROR identisch ist), und MCSVC übergibt den zurückgegebenen Wert zur Verarbeitung zurück an \_ den NPP.

Wenn die Methode nicht erfolgreich ist, geben Sie einen Fehlercode zurück. Bei einem Fehler übergibt MCSVC den zurückgegebenen Wert zur Verarbeitung zurück an das NPP.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




