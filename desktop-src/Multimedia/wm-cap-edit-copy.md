---
title: WM_CAP_EDIT_COPY-Nachricht (Vfw.h)
description: Die \_ WM CAP \_ EDIT \_ COPY-Nachricht kopiert den Inhalt des Videoframepuffers und der zugeordneten Palette in die Zwischenablage. Sie können diese Nachricht explizit oder mithilfe des CapEditCopy-Makros senden.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- WM_CAP_EDIT_COPY nachricht Windows Multimedia
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
ms.openlocfilehash: e944273ff8519aefa52803b2072199760a480e0fcb2a76dd314b578dcbcfdf4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892080"
---
# <a name="wm_cap_edit_copy-message"></a>WM \_ CAP \_ EDIT \_ COPY-Nachricht

Die **WM CAP EDIT \_ \_ \_ COPY-Nachricht** kopiert den Inhalt des Videoframepuffers und der zugeordneten Palette in die Zwischenablage. Sie können diese Nachricht explizit oder mithilfe des [**CapEditCopy-Makros**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) senden.


```C++
WM_CAP_EDIT_COPY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> <dt>

[Video Capture Messages](video-capture-messages.md)
</dt> </dl>

 

 





