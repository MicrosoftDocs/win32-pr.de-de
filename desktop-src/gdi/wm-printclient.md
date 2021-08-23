---
description: Die WM \_ PRINTCLIENT-Nachricht wird an ein Fenster gesendet, um anzufordern, dass der Clientbereich im angegebenen Gerätekontext gezeichnet wird, am häufigsten in einem Druckergerätekontext.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: WM_PRINTCLIENT Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807c12ca4d0a5fe5f1e2a12aecd3b3148d936119f72771e811fe85d5b0af3abf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717660"
---
# <a name="wm_printclient-message"></a>WM \_ PRINTCLIENT-Nachricht

Die **WM \_ PRINTCLIENT-Nachricht** wird an ein Fenster gesendet, um anzufordern, dass der Clientbereich im angegebenen Gerätekontext gezeichnet wird, am häufigsten in einem Druckergerätekontext.

Im Gegensatz zu [**WM \_ PRINT**](wm-print.md)wird **WM \_ PRINTCLIENT** nicht von [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)verarbeitet. Ein Fenster sollte die **WM \_ PRINTCLIENT-Nachricht** über eine anwendungsdefinierte [**WindowProc-Funktion**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) verarbeiten, damit sie ordnungsgemäß verwendet werden kann.


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

Ein Handle für den Gerätekontext, der gezeichnet werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Zeichnungsoptionen. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                  | Bedeutung                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**PRF \_ CHECKVISIBLE**</dt> </dl> | Zeichnet das Fenster nur, wenn es sichtbar ist.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**PRF \_ CHILDREN**</dt> </dl>             | Zeichnet alle sichtbaren untergeordneten Fenster.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**\_PRF-CLIENT**</dt> </dl>                   | Zeichnet den Clientbereich des Fensters.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**PRF \_ ERASEBKGND**</dt> </dl>       | Löscht den Hintergrund vor dem Zeichnen des Fensters.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**PRF \_ NONCLIENT**</dt> </dl>          | Zeichnet den Nicht-Clientbereich des Fensters.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**PRF \_ OWNED**</dt> </dl>                      | Zeichnet alle eigenen Fenster.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Fenster kann diese Meldung in etwa auf die gleiche Weise verarbeiten wie [**WM \_ PAINT,**](./wm-paint.md)mit der Ausnahme, dass [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) und [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) nicht aufgerufen werden müssen (ein Gerätekontext wird bereitgestellt), und das Fenster sollte seinen gesamten Clientbereich anstatt nur den ungültigen Bereich zeichnen.

Windows, die überall im System verwendet werden können, z. B. Steuerelemente, sollten diese Meldung verarbeiten. Es ist wahrscheinlich sinnvoll, diese Meldung auch in anderen Fenstern zu verarbeiten, da sie relativ einfach zu implementieren ist.

Die [AnimateWindow-Funktion](/windows/desktop/api/winuser/nf-winuser-animatewindow) erfordert, dass das animierte Fenster die **WM \_ PRINTCLIENT-Nachricht** implementiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Zeichnen und Zeichnen](painting-and-drawing.md)
</dt> <dt>

[Zeichnen und Zeichnen von Nachrichten](painting-and-drawing-messages.md)
</dt> <dt>

[**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**WM \_ PAINT**](wm-paint.md)
</dt> </dl>

 

 
