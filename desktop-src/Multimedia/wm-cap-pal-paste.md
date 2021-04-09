---
title: WM_CAP_PAL_PASTE Meldung (VFW. h)
description: Die WM \_ \_ -Cap \_ -PAL-Einfüge Nachricht kopiert die Palette aus der Zwischenablage und übergibt sie an einen Aufzeichnungs Treiber. Sie können diese Nachricht explizit oder mithilfe des cappalettepaste-Makros senden.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- WM_CAP_PAL_PASTE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3daf88c69edbb8bad6257456b95a86c8a68df328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949677"
---
# <a name="wm_cap_pal_paste-message"></a>WM- \_ Obergrenze für \_ PAL- \_ Einfügen

Die **WM- \_ Cap-PAL- \_ \_ Einfüge** Nachricht kopiert die Palette aus der Zwischenablage und übergibt sie an einen Aufzeichnungs Treiber. Sie können diese Nachricht explizit oder mithilfe des [**cappalettepaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) -Makros senden.


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

Wenn ein Fehler auftritt und eine Fehler Rückruffunktion mithilfe der WM- [**\_ Cap- \_ \_ Rückruf \_ Fehlermeldung**](wm-cap-set-callback-error.md) festgelegt wird, wird die Fehler Rückruffunktion aufgerufen.

## <a name="remarks"></a>Bemerkungen

Ein Aufzeichnungs Treiber verwendet eine Palette, wenn dies für das angegebene digitalisierte Videoformat erforderlich ist.

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

 

 





