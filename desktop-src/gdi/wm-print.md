---
description: Die WM PRINT-Nachricht wird an ein Fenster gesendet, um an fordern, sich selbst im angegebenen Gerätekontext zu zeichnen, am häufigsten in einem \_ Druckergerätekontext.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: WM_PRINT (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09d3cb7dbb3b4a4fca7a2af4272f1b4175aa26e911d1def909c97ba35f3d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964850"
---
# <a name="wm_print-message"></a>WM \_ PRINT-Meldung

Die **WM \_ PRINT-Nachricht** wird an ein Fenster gesendet, um an fordern, sich selbst im angegebenen Gerätekontext zu zeichnen, am häufigsten in einem Druckergerätekontext.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Zu zeichnenden Gerätekontext.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Zeichnungsoptionen. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                  | Bedeutung                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**PRF \_ CHECKVISIBLE**</dt> </dl> | Zeichnet das Fenster nur, wenn es sichtbar ist.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**PRF \_ CHILDREN**</dt> </dl>             | Zeichnet alle sichtbaren Fenster für die unteren Fenster.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**\_PRF-CLIENT**</dt> </dl>                   | Zeichnet den Clientbereich des Fensters.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**PRF \_ ERASEBKGND**</dt> </dl>       | Löscht den Hintergrund vor dem Zeichnen des Fensters.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**PRF \_ NONCLIENT**</dt> </dl>          | Zeichnet den Nicht-Clientbereich des Fensters.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**PRF \_ OWNED**</dt> </dl>                      | Zeichnet alle fenstereigenen Fenster.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) verarbeitet diese Meldung basierend auf der angegebenen Zeichnungsoption: , wenn PRF CHECKVISIBLE angegeben ist und das Fenster nicht sichtbar ist. Nichts tun, wenn PRF NONCLIENT angegeben ist, zeichnen Sie den Nichtclientbereich im angegebenen Gerätekontext. Wenn PRF ERASEBKGND angegeben ist, senden Sie dem Fenster eine \_ WM \_ \_ [**\_ ERASEBKGND-Nachricht.**](../winmsg/wm-erasebkgnd.md) Wenn PRF CLIENT angegeben ist, senden Sie dem Fenster eine \_ WM [**\_ PRINTCLIENT-Nachricht.**](wm-printclient.md) Wenn PRF CHILDREN festgelegt ist, senden Sie jedem sichtbaren untergeordneten Fenster eine \_ WM **\_ PRINT-Nachricht,** wenn PRF OWNED festgelegt ist, senden Sie jedem sichtbaren eigenen Fenster eine WM \_ **\_ PRINT-Nachricht.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Das Zeichnen und Zeichnen](painting-and-drawing.md)
</dt> <dt>

[Zeichnen und Zeichnen von Nachrichten](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM \_ PRINTCLIENT**](wm-printclient.md)
</dt> </dl>

 

 
