---
title: WM_CONTEXTMENU Meldung (Winuser. h)
description: Benachrichtigt ein Fenster, dass der Benutzer im Fenster auf die Rechte Maustaste geklickt hat (Rechtsklick).
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7764926709bfc8ab6aa95be330a9d45d38bc48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338142"
---
# <a name="wm_contextmenu-message"></a>WM- \_ ContextMenu-Meldung

Benachrichtigt ein Fenster, dass der Benutzer ein Kontextmenü anzeigen möchte.  Der Benutzer hat möglicherweise im Fenster auf die Rechte Maustaste geklickt (mit der rechten Maustaste geklickt), die UMSCHALTTASTE + F10 gedrückt oder den Anwendungs Schlüssel (Kontextmenü Taste) gedrückt, der auf einigen Tastaturen verfügbar ist.


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, in dem der Benutzer mit der rechten Maustaste auf die Maus geklickt hat. Dies kann ein untergeordnetes Fenster des Fensters sein, in dem die Nachricht empfangen wird. Weitere Informationen zum Verarbeiten dieser Nachricht finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*lParam* 
</dt> <dd>

Mit dem nieder wertigen Wort wird die horizontale Position des Cursors in Bildschirm Koordinaten zum Zeitpunkt der Mausklicks angegeben.

Das höchst wertige Wort gibt die vertikale Position des Cursors in Bildschirm Koordinaten zum Zeitpunkt der Mausklicks an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Diese Meldung kann von einem Fenster verarbeitet werden, indem ein Kontextmenü mithilfe der [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) -Funktion oder der [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) -Funktion angezeigt wird. Verwenden Sie den folgenden Code zum Abrufen der horizontalen und vertikalen Positionen.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Wenn ein Fenster kein Kontextmenü anzeigt, sollte es diese Meldung an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben. Wenn es sich bei einem Fenster um ein untergeordnetes Fenster handelt, sendet **defwindowproc** die Nachricht an das übergeordnete Element. Andernfalls zeigt **defwindowproc** ein Standardkontext Menü an, wenn die angegebene Position in der Beschriftung des Fensters angezeigt wird.

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) generiert bei der Verarbeitung der " [**WM \_ rbuttonup**](/windows/desktop/inputdev/wm-rbuttonup) "-oder " [**WM \_ ncrbuttonup**](/windows/desktop/inputdev/wm-ncrbuttonup) "-Meldung die WM-Meldung " **\_ ContextMenu** ", oder wenn der Benutzer UMSCHALT + F10 eingibt. Die " **WM \_ ContextMenu** "-Meldung wird auch generiert, wenn der Benutzer den Schlüssel " [**VK \_ apps**](/windows/desktop/inputdev/virtual-key-codes) " drückt und freigibt.

Wenn das Kontextmenü z. b. aus der Tastatur generiert wird, wenn der Benutzer UMSCHALT + F10 eingibt, sind die x-und y-Koordinaten-1, und die Anwendung sollte das Kontextmenü an der Position der aktuellen Auswahl anstelle von (xpos, ypos) anzeigen.

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

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**\_Y- \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[**WM- \_ ncrbuttonup**](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[**WM- \_ rbuttonup**](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

**Licher**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

