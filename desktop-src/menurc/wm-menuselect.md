---
title: WM_MENUSELECT Meldung (Winuser. h)
description: Wird an das Besitzer Fenster eines Menüs gesendet, wenn der Benutzer ein Menü Element auswählt.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342675"
---
# <a name="wm_menuselect-message"></a>WM- \_ MenuSelect-Meldung

Wird an das Besitzer Fenster eines Menüs gesendet, wenn der Benutzer ein Menü Element auswählt.


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das nieder wertige Wort gibt das Menü Element oder den unter Menü Index an. Wenn das ausgewählte Element ein Befehls Element ist, enthält dieser Parameter den Bezeichner des Menü Elements. Wenn das ausgewählte Element ein Dropdown Menü oder ein Untermenü öffnet, enthält dieser Parameter den Index des Dropdown Menüs oder des Untermenüs im Hauptmenü, und der *LPARAM* -Parameter enthält das Handle für das Hauptmenü (geklickt). Verwenden Sie die [**getsubmenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) -Funktion, um das Menü Handle im Dropdown Menü oder Untermenü zu erhalten.

Das höchst wertige Wort gibt mindestens ein menüflags an. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                             | Bedeutung                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <dt>**MF \_ Bitmap**</dt> <dt>0x00000004l</dt> </dl>                | Element zeigt eine Bitmap an.<br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <dt>**MF \_**</dt> <dt>0x00000008l</dt> wurde geprüft. </dl>             | Das Element ist aktiviert.<br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <dt>**MF \_**</dt> <dt>0x00000002l</dt> deaktiviert </dl>          | Element ist deaktiviert.<br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <dt>**MF \_**</dt>Abgeblendet <dt>0x00000001l</dt> </dl>                | Das Element ist ausgegraut.<br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <dt>**MF \_ Hilite**</dt> <dt>0x00000080l</dt> </dl>                | Das Element ist hervorgehoben.<br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <dt>**MF \_ Mouseselect**</dt> <dt>0x00008000l</dt> </dl> | Das Element wird mit der Maus ausgewählt.<br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <dt>**MF \_ Besitzdraw**</dt> <dt>0x00000100l</dt> </dl>       | Item ist ein vom Besitzer gezeichnetes Element.<br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ Popup**</dt> <dt>0x00000010l</dt> </dl>                   | Element öffnet ein Dropdown Menü oder ein Untermenü.<br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ Sysmenu**</dt> <dt>0x00002000l</dt> </dl>             | Das Element ist im Menü Fenster enthalten. Der *LPARAM* -Parameter enthält ein Handle für das Menü, das der Nachricht zugeordnet ist.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Menü, auf das geklickt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Wenn das hochwertige Wort von *wParam* den Wert 0xFFFF enthält und der *LPARAM* -Parameter **null** enthält, hat das System das Menü geschlossen.

Verwenden Sie nicht den Wert 1 für das hochwertige Wort von *wParam*, da dieser Wert als (**uint**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*) angegeben wird. Wenn der Wert 0xFFFF ist, wird er aufgrund der Umwandlung in einen **uint** als 0X0000FFFF, nicht als 1 interpretiert.

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

[**Getsubmenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Licher**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

