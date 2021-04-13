---
title: WM_ENTERIDLE Meldung (Winuser. h)
description: Wird an das Besitzer Fenster eines modalen Dialog Felds oder Menüs gesendet, das in den Leerlaufzustand wechselt. Ein modales Dialogfeld oder Menü wechselt in den Leerlaufzustand, wenn keine Nachrichten in der Warteschlange warten, nachdem mindestens eine vorherige Nachricht verarbeitet wurde.
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- Dialog Felder WM_ENTERIDLE Meldung
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99b3150a0dbc1a81b78498c8e295fbf2397c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392101"
---
# <a name="wm_enteridle-message"></a>WM-Enterprise- \_ Nachricht

Wird an das Besitzer Fenster eines modalen Dialog Felds oder Menüs gesendet, das in den Leerlaufzustand wechselt. Ein modales Dialogfeld oder Menü wechselt in den Leerlaufzustand, wenn keine Nachrichten in der Warteschlange warten, nachdem mindestens eine vorherige Nachricht verarbeitet wurde.


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                   | Bedeutung                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <dt>**MSGF \_ Dialogbox**</dt> <dt>0</dt> </dl> | Das System befindet sich im Leerlauf, weil ein Dialogfeld angezeigt wird.<br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <dt>**MSGF \_ Menü**</dt> <dt>2</dt> </dl>                | Das System befindet sich im Leerlauf, weil ein Menü angezeigt wird.<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Dialogfeld (wenn *wParam* das **MSGF- \_ Dialogfeld** ist) oder ein Fenster mit dem angezeigten Menü (wenn *wParam* das **MSGF- \_ Menü** ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Wenn Sie das Dialogfeld mit dem Format " **DS \_ noidlemsg** " erstellen, können Sie die " **WM \_ Enter inidle** "-Meldung für ein Dialogfeld unterdrücken.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Licher**
</dt> <dt>

[Dialog Felder](dialog-boxes.md)
</dt> </dl>

 

