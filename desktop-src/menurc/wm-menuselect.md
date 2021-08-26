---
title: WM_MENUSELECT Meldung (Winuser.h)
description: Wird an das Besitzerfenster eines Menüs gesendet, wenn der Benutzer ein Menüelement auswählt.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT Meldung Menüs und andere Ressourcen
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
ms.openlocfilehash: 1708aabf8ea12bf20c919f1306672358c2966a3d23aa0badccb1f4592c543f3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952220"
---
# <a name="wm_menuselect-message"></a>WM \_ MENUSELECT-Meldung

Wird an das Besitzerfenster eines Menüs gesendet, wenn der Benutzer ein Menüelement auswählt.


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt das Menüelement oder den Untermenüindex an. Wenn das ausgewählte Element ein Befehlselement ist, enthält dieser Parameter den Bezeichner des Menüelements. Wenn das ausgewählte Element ein Dropdownmenü oder Untermenü öffnet, enthält dieser Parameter den Index des Dropdownmenüs oder des Untermenüs im Hauptmenü, und der *Parameter lParam* enthält das Handle für das Hauptmenü (geklickt). Verwenden Sie die [**GetSubMenu-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) um das Menühandle zum Dropdownmenü oder Untermenü abzurufen.

Das Wort in hoher Reihenfolge gibt ein oder mehrere Menüflags an. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                                                                             | Bedeutung                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <dt>**MF \_ BITMAP**</dt> <dt>0x00000004L</dt> </dl>                | Element zeigt eine Bitmap an.<br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <dt>**MF \_ CHECKED**</dt> <dt>0x00000008L</dt> </dl>             | Das Element ist aktiviert.<br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <dt>**MF \_ DISABLED**</dt> <dt>0x00000002L</dt> </dl>          | Element ist deaktiviert.<br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <dt>**MF \_ GRAYED**</dt> <dt>0x00000001L</dt> </dl>                | Das Element ist abgeblendet.<br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <dt>**MF \_ HILITE**</dt> <dt>0x00000080L</dt> </dl>                | Das Element ist hervorgehoben.<br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <dt>**MF \_ MOUSESELECT**</dt> <dt>0x00008000L</dt> </dl> | Das Element wird mit der Maus ausgewählt.<br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <dt>**MF \_ OWNERDRAW**</dt> <dt>0x00000100L</dt> </dl>       | Das Element ist ein vom Besitzer gezeichnetes Element.<br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x00000010L</dt> </dl>                   | Das Element öffnet ein Dropdownmenü oder Untermenü.<br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl>             | Das Element ist im Fenstermenü enthalten. Der *lParam-Parameter* enthält ein Handle für das Menü, das der Nachricht zugeordnet ist.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Menü, auf das geklickt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Wenn das Wort in hoher Reihenfolge von *wParam* 0xFFFF enthält und der *lParam-Parameter* **NULL** enthält, hat das System das Menü geschlossen.

Verwenden Sie nicht den Wert 1 für das Wort der hohen Ordnung von *wParam,* da dieser Wert als (**UINT**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*) angegeben ist. Wenn der Wert 0xFFFF ist, wird er aufgrund der Umwandlung in einen **UINT** als 0x0000FFFF und nicht als 1 interpretiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Tastaturkürzel](keyboard-accelerators.md)
</dt> </dl>

 

