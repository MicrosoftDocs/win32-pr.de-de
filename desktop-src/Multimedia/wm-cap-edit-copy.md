---
title: WM_CAP_EDIT_COPY Meldung (VFW. h)
description: Die " \_ WM \_ \_ -Cap-Kopier Nachricht bearbeiten" kopiert den Inhalt des Video Frame Puffers und der zugehörigen Palette in die Zwischenablage. Sie können diese Nachricht explizit oder mithilfe des capeditcopy-Makros senden.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- WM_CAP_EDIT_COPY-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104702"
---
# <a name="wm_cap_edit_copy-message"></a>\_Meldung zum \_ Bearbeiten der WM-Abdeckung \_

Die " **WM-Cap- \_ \_ \_ Kopier Nachricht bearbeiten** " kopiert den Inhalt des Video Frame Puffers und der zugehörigen Palette in die Zwischenablage. Sie können diese Nachricht explizit oder mithilfe des [**capeditcopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) -Makros senden.


```C++
WM_CAP_EDIT_COPY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

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

 

 





