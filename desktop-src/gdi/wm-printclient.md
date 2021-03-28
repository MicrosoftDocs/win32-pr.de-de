---
description: Die WM- \_ printclient-Nachricht wird an ein Fenster gesendet, um anzufordern, dass Sie den Client Bereich im angegebenen Gerätekontext (in der Regel in einem Drucker Gerätekontext) zeichnet.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: WM_PRINTCLIENT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52aca68695964a35ab9a2c4e309cd71c2e9f7eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980280"
---
# <a name="wm_printclient-message"></a>WM- \_ printclient-Meldung

Die **WM- \_ printclient** -Nachricht wird an ein Fenster gesendet, um anzufordern, dass Sie den Client Bereich im angegebenen Gerätekontext (in der Regel in einem Drucker Gerätekontext) zeichnet.

Im Gegensatz zum [**WM- \_ Print**](wm-print.md)wird **WM \_ printclient** nicht von [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)verarbeitet. Ein Fenster sollte die **WM \_ printclient** -Nachricht über eine von der Anwendung definierte [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion verarbeiten, damit es ordnungsgemäß verwendet werden kann.


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

Diese Nachricht kann von einem Fenster auf die gleiche Weise wie bei [**WM \_ Paint**](./wm-paint.md)verarbeitet werden, mit der Ausnahme, dass [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) und [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) nicht aufgerufen werden müssen (ein Gerätekontext wird bereitgestellt) und das Fenster den gesamten Client Bereich und nicht nur den ungültigen Bereich zeichnen soll.

Windows, die an beliebiger Stelle im System verwendet werden können, z. b. Steuerelemente, sollten diese Nachricht verarbeiten. Es ist wahrscheinlich auch für andere Fenster sinnvoll, diese Nachricht zu verarbeiten, da Sie relativ einfach zu implementieren ist.

Die [animatewindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) -Funktion erfordert, dass das zu animierende Fenster die **WM \_ printclient** -Nachricht implementiert.

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

[**Animatewindow**](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**Endpaint auf**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**WM- \_ Paint**](wm-paint.md)
</dt> </dl>

 

 
