---
title: ICM_SET_STATUS_PROC Meldung (VFW. h)
description: Die ICM \_ Set \_ Status \_ proc-Nachricht stellt eine Status Rückruffunktion mit dem Status eines langwierigen Vorgangs bereit.
ms.assetid: a1bcd840-b94b-487e-91d6-67411a8a3a2d
keywords:
- ICM_SET_STATUS_PROC-Nachricht (Multimedia)
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
ms.openlocfilehash: 53d7ad2745ab53c2e04a1588ddbf1b1e5d755202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479389"
---
# <a name="icm_set_status_proc-message"></a>ICM \_ - \_ Status-proc- \_ Nachricht

Die **ICM \_ Set \_ Status \_ proc** -Nachricht stellt eine Status Rückruffunktion mit dem Status eines langwierigen Vorgangs bereit.


```C++
ICM_SET_STATUS_PROC 
wParam = (DWORD_PTR)icsetstatusProc; 
lParam = sizeof(ICSETSTATUSPROC); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="icsetstatusProc"></span><span id="icsetstatusproc"></span><span id="ICSETSTATUSPROC"></span>*icsetstatusproc*
</dt> <dd>

Zeiger auf eine [**icsetstatusproc**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc) -Struktur.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Größe von **icsetstatusproc** in Byte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei erfolgreicher Ausführung von ICERR \_ OK oder andernfalls einen Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Die Unterstützung dieser Nachricht ist optional, wird jedoch dringend empfohlen, wenn die Komprimierung oder Dekomprimierung länger als ungefähr eine Zehntelsekunde dauert.

Eine Anwendung kann diese Nachricht in regelmäßigen Abständen an eine Status Rückruffunktion senden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> <dt>

[Video Komprimierungs Meldungen](video-compression-messages.md)
</dt> </dl>

 

 





