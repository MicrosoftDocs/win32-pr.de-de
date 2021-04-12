---
title: WM_CAP_ABORT Meldung (VFW. h)
description: Die WM \_ - \_ Abbruchs Nachricht beendet den Aufzeichnungs Vorgang.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- WM_CAP_ABORT-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517723"
---
# <a name="wm_cap_abort-message"></a>\_ \_ Abbruch Meldung für WM-Cap

Die **WM \_ - \_ Abbruchs** Nachricht beendet den Aufzeichnungs Vorgang. Bei der Schritt Erfassung werden die Abbild Daten, die bis zum Zeitpunkt der WM- **\_ \_ Abbruchs** Nachricht erfasst werden, in der Erfassungs Datei aufbewahrt, die Audiodaten werden jedoch nicht erfasst. Sie können diese Nachricht explizit oder mithilfe des [**capcaptureabort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) -Makros senden.


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Der Aufzeichnungs Vorgang muss durchführen, um diese Meldung zu verwenden.

Verwenden Sie die Stop-Nachricht der [**WM- \_ Obergrenze \_**](wm-cap-stop.md) , um die Schritt Erfassung an der aktuellen Position anzuhalten und dann Audiodaten aufzuzeichnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> <dt>

[Video Erfassungs Meldungen](video-capture-messages.md)
</dt> </dl>

 

 





