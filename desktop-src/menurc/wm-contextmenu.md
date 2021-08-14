---
title: WM_CONTEXTMENU (Winuser.h)
description: Benachrichtigt ein Fenster, dass der Benutzer im Fenster mit der rechten Maustaste (rechtsklickt) geklickt hat.
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU von Nachrichtenmenüs und anderen Ressourcen
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
ms.openlocfilehash: 0c036bf0711f208bae25657d572102a7f4d82525076ee1d0b6f4ebd6598e8197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472505"
---
# <a name="wm_contextmenu-message"></a>WM \_ CONTEXTMENU-Nachricht

Benachrichtigt ein Fenster, dass ein Kontextmenü angezeigt werden soll.  Möglicherweise hat der Benutzer im Fenster mit der rechten Maustaste (mit der rechten Maustaste) geklickt, UMSCHALT+F10 gedrückt oder die Anwendungstaste (Kontextmenütaste) gedrückt, die auf einigen Tastaturen verfügbar ist.


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für das Fenster, in dem der Benutzer mit der rechten Maustaste auf die Maus geklickt hat. Dies kann ein untergeordnetes Fenster des Fensters sein, das die Nachricht empfängt. Weitere Informationen zum Verarbeiten dieser Nachricht finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt die horizontale Position des Cursors in Bildschirmkoordinaten zum Zeitpunkt des Mausklicks an.

Das obere Wort gibt die vertikale Position des Cursors in Bildschirmkoordinaten zum Zeitpunkt des Mausklicks an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Ein Fenster kann diese Meldung verarbeiten, indem ein Kontextmenü mithilfe der [**Funktionen TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) oder [**TrackPopupMenuEx angezeigt**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) wird. Verwenden Sie den folgenden Code, um die horizontalen und vertikalen Positionen zu erhalten.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Wenn in einem Fenster kein Kontextmenü angezeigt wird, sollte diese Meldung an die [**DefWindowProc-Funktion übergeben**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) werden. Wenn ein Fenster ein untergeordnetes Fenster ist, **sendet DefWindowProc** die Nachricht an das übergeordnete Fenster. **Andernfalls zeigt DefWindowProc** ein Standardverknüpfungsmenü an, wenn sich die angegebene Position in der Beschriftung des Fensters befindet.

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) generiert die **WM \_ CONTEXTMENU-Nachricht,** wenn die [**WM \_ RBUTTONUP-**](/windows/desktop/inputdev/wm-rbuttonup) oder [**WM \_ NCRBUTTONUP-Nachricht**](/windows/desktop/inputdev/wm-ncrbuttonup) verarbeitet wird oder wenn der Benutzer UMSCHALT+F10 ein gibt. Die **WM \_ CONTEXTMENU-Meldung** wird auch generiert, wenn der Benutzer den [**\_ VK-APPS-Schlüssel**](/windows/desktop/inputdev/virtual-key-codes) drückt und frei gibt.

Wenn das Kontextmenü beispielsweise über die Tastatur generiert wird, wenn der Benutzer UMSCHALT+F10 eint, sind die x- und y-Koordinaten -1, und die Anwendung sollte das Kontextmenü an der Position der aktuellen Auswahl statt an (xPos, yPos) anzeigen.

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

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**Trackpopupmenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

