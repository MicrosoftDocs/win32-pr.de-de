---
description: Eine Anwendung sendet die WM \_ setredraw-Nachricht an ein Fenster, damit Änderungen in diesem Fenster neu gezeichnet werden können, oder um zu verhindern, dass Änderungen in diesem Fenster neu gezeichnet werden.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: WM_SETREDRAW Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217039"
---
# <a name="wm_setredraw-message"></a>WM- \_ Nachricht "abzeichnen"

Eine Anwendung sendet die **WM \_ setredraw** -Nachricht an ein Fenster, damit Änderungen in diesem Fenster neu gezeichnet werden können, oder um zu verhindern, dass Änderungen in diesem Fenster neu gezeichnet werden.

Um diese Nachricht zu senden, wenden Sie die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion mit den folgenden Parametern an.


```C++
SendMessage( 
  (HWND) hWnd,              
  WM_SETREDRAW,             
  (WPARAM) wParam,          
  (LPARAM) lParam            
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der neu zeichnen-Zustand. Wenn dieser Parameter **true** ist, kann der Inhalt nach einer Änderung neu gezeichnet werden. Wenn dieser Parameter **false** ist, kann der Inhalt nach einer Änderung nicht neu gezeichnet werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung gibt 0 (null) zurück, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Diese Meldung kann nützlich sein, wenn eine Anwendung mehrere Elemente zu einem Listenfeld hinzufügen muss. Die Anwendung kann diese Nachricht mit dem Wert " **false**" von *wParam* abrufen, die Elemente hinzufügen und die Nachricht dann erneut aufzurufen, wobei *wParam* auf " **true**" festgelegt ist. Zum Schluss kann die Anwendung [**redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)aufrufen (*HWND*, **null**, **null**, RDW \_ Erase \| RDW- \_ Frame \| RDW \_ Invalidate \| RDW \_ AllChildren), damit das Listenfeld neu gezeichnet wird.

> [!Note]  
> Das redrawwindow-Element mit den angegebenen Flags wird anstelle von [**invalidatererenverwendet**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) , da das erste-Steuerelement für einige Steuerelemente erforderlich ist, die nicht über einen Client Bereich verfügen, oder über Fenster Stile verfügen, die bewirken, dass Sie einen nicht-Client Bereich erhalten (z. b. **WS- \_ thickframe** [](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) , **WS \_**-Rahmen oder **WS \_ Ex \_ clientedge** Wenn das Steuerelement nicht über einen nicht-Client Bereich verfügt, führt **redrawwindow** mit diesen Flags nur so viele ungültige Invalidierung durch wie **invalidaten.**

 

Wenn die Anwendung die **WM \_ setredraw** -Nachricht an ein ausgeblendetes Fenster sendet, wird das Fenster sichtbar (d. h., das Betriebssystem fügt dem Fenster das **\_ sichtbare WS** -Format hinzu).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über das Zeichnen und zeichnen](painting-and-drawing.md)
</dt> <dt>

[Zeichnen und Zeichnen von Nachrichten](painting-and-drawing-messages.md)
</dt> <dt>

[**Redrawwindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 
