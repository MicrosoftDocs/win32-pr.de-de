---
description: Die WM- \_ Druck Meldung wird an ein Fenster gesendet, um anzufordern, dass Sie sich im angegebenen Gerätekontext befindet, in der Regel in einem Drucker Gerätekontext.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: WM_PRINT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042117"
---
# <a name="wm_print-message"></a>WM- \_ Druck Meldung

Die **WM- \_ Druck** Meldung wird an ein Fenster gesendet, um anzufordern, dass Sie sich im angegebenen Gerätekontext befindet, in der Regel in einem Drucker Gerätekontext.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

Ein Handle für den Gerätekontext, in dem gezeichnet werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Zeichnungsoptionen. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                  | Bedeutung                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**PRF \_ checkvisible**</dt> </dl> | Zeichnet das Fenster nur, wenn es sichtbar ist.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**untergeordnete Elemente \_**</dt> </dl>             | Zeichnet alle sichtbaren untergeordneten Fenster.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**PRF- \_ Client**</dt> </dl>                   | Zeichnet den Client Bereich des Fensters.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**PRF \_ erasebkgnd**</dt> </dl>       | Löscht den Hintergrund vor dem Zeichnen des Fensters.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**PRF- \_ nonclient**</dt> </dl>          | Zeichnet den nicht-Client Bereich des Fensters.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**PRF- \_ Besitzer**</dt> </dl>                      | Zeichnet alle eigenen Fenster.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion verarbeitet diese Nachricht auf der Grundlage der angegebenen Zeichnungs Option: Wenn PRF \_ checkvisible angegeben und das Fenster nicht sichtbar ist, führen Sie Nothing aus, wenn PRF- \_ nicht angegeben ist, den nicht-Client Bereich im angegebenen Gerätekontext zeichnen. wenn PRF \_ erasebkgnd angegeben ist, senden Sie das Fenster eine [**WM \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) -Meldung, wenn der PRF- \_ Client angegeben ist, das Fenster eine [**WM \_ printclient**](wm-printclient.md) -Nachricht senden, wenn PRF-untergeordnete \_ Fenster festgelegt ist, jedes sichtbare untergeordnete Fenster an eine **WM- \_ Druck** Nachricht senden, wenn PRF- \_ Besitzer festgelegt ist. **\_**

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM- \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM- \_ printclient**](wm-printclient.md)
</dt> </dl>

 

 
