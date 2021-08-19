---
title: WM_ENTERIDLE (Winuser.h)
description: Wird an das Besitzerfenster eines modalen Dialogfelds oder Menüs gesendet, das in den Leerlaufzustand über geht. Ein modales Dialogfeld oder Menü befindet sich in einem Leerlaufzustand, wenn keine Nachrichten in der Warteschlange warten, nachdem eine oder mehrere vorherige Nachrichten verarbeitet wurden.
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- WM_ENTERIDLE-Dialogfelder
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
ms.openlocfilehash: 0fb7d40ae84659d1cfad12357956c4a955ae4f879cddcc13b51069a6a62cd08c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985280"
---
# <a name="wm_enteridle-message"></a>WM \_ ENTERIDLE-Meldung

Wird an das Besitzerfenster eines modalen Dialogfelds oder Menüs gesendet, das in den Leerlaufzustand über geht. Ein modales Dialogfeld oder Menü befindet sich in einem Leerlaufzustand, wenn keine Nachrichten in der Warteschlange warten, nachdem eine oder mehrere vorherige Nachrichten verarbeitet wurden.


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
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <dt>**MSGF \_ DIALOGBOX**</dt> <dt>0</dt> </dl> | Das System befindet sich im Leerlauf, da ein Dialogfeld angezeigt wird.<br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <dt>**MSGF \_ MENÜ**</dt> <dt>2</dt> </dl>                | Das System befindet sich im Leerlauf, da ein Menü angezeigt wird.<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Dialogfeld (wenn *wParam* **MSGF \_ DIALOGBOX** ist) oder das Fenster, das das angezeigte Menü enthält (wenn *wParam* **MSGF \_ MENU ist).**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Sie können die **WM \_ ENTERIDLE-Meldung** für ein Dialogfeld unterdrücken, indem Sie das Dialogfeld mit dem **DS \_ NOIDLEMSG-Format** erstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Dialogfelder](dialog-boxes.md)
</dt> </dl>

 

