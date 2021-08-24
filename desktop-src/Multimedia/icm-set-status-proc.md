---
title: ICM_SET_STATUS_PROC (Vfw.h)
description: Die ICM \_ SET \_ STATUS \_ PROC-Nachricht stellt eine Statusrückruffunktion mit dem Status eines längeren Vorgangs zur Veranschlagung.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- ICM_SET_STATUS_PROC-Nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_SET_STATUS_PROC
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02019bb6375aa18fd37ba34d2603839b37291d58822858b0b9cabc01e47d7b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678340"
---
# <a name="icm_set_status_proc-message"></a>\_ICM SET \_ STATUS \_ PROC-Meldung

Die **ICM SET STATUS \_ \_ \_ PROC** enthält eine Statusrückruffunktion mit dem Status eines längeren Vorgangs.


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusProc*
</dt> <dd>

Zeiger auf eine [**ICSETSTATUSPROC-Struktur.**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Größe von **ICSETSTATUSPROC** in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ICERR \_ OK zurück, wenn erfolgreich oder andernfalls ein Fehler aufgetreten ist.

## <a name="remarks"></a>Hinweise

Die Unterstützung dieser Meldung ist optional, wird jedoch dringend empfohlen, wenn die Komprimierung oder Dekomprimierung länger als etwa ein Zehntel einer Sekunde dauert.

Eine Anwendung kann diese Nachricht bei längeren Vorgängen in regelmäßigen Abständen an eine Statusrückruffunktion senden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Videokomprimierungsmeldungen](video-compression-messages.md)
</dt> </dl>

 

 





