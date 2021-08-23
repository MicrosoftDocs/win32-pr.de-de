---
title: WM_NCXBUTTONDOWN (Winuser.h)
description: Wird veröffentlicht, wenn der Benutzer die erste oder zweite X-Schaltfläche drückt, während sich der Cursor im Nicht-Clientbereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gesendet.
ms.assetid: 72744c98-1898-4548-bd10-61ad53eeab15
keywords:
- WM_NCXBUTTONDOWN der Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17097748b064fe125bac20240f14684dfe01b560485c926e36e868da223e7d7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666260"
---
# <a name="wm_ncxbuttondown-message"></a>WM \_ NCXBUTTONDOWN-Meldung

Wird veröffentlicht, wenn der Benutzer die erste oder zweite X-Schaltfläche drückt, während sich der Cursor im Nicht-Clientbereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese *Meldung* nicht gesendet.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCXBUTTONDOWN                0x00AB
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt den Treffertestwert an, der von der [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) bei der Verarbeitung der [**WM \_ NCHITTEST-Nachricht zurückgegeben**](wm-nchittest.md) wird. Eine Liste der Treffertestwerte finden Sie unter **WM \_ NCHITTEST**. Das obere Wort gibt an, welche Schaltfläche gedrückt wurde. Dieses Argument einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                     | Bedeutung                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1-0x0001**</dt> <dt></dt> </dl> | Die erste X-Schaltfläche wurde gedrückt.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2-0x0002**</dt> <dt></dt> </dl> | Die zweite X-Schaltfläche wurde gedrückt.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**POINTS-Struktur,**](/previous-versions//dd162808(v=vs.85)) die die x- und y-Koordinaten des Cursors enthält. Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie **TRUE zurückgeben.** Weitere Informationen zur Verarbeitung des Rückgabewerts finden Sie im Abschnitt Hinweise.

## <a name="remarks"></a>Hinweise

Verwenden Sie den folgenden Code, um die Informationen im *wParam-Parameter* zu erhalten.


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



Sie können auch den folgenden Code verwenden, um die x- und y-Koordinaten aus *lParam zu erhalten:*


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Verwenden Sie nicht die [**LOWORD-**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) oder [**HIWORD-Makros,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) um die x- und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse auf Systemen mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können negative x- und y-Koordinaten haben, **und LOWORD** und **HIWORD** behandeln die Koordinaten als Mengen ohne Vorzeichen.

 

Standardmäßig testet die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) den angegebenen Punkt, um die Position des Cursors zu erhalten, und führt die entsprechende Aktion aus. Gegebenenfalls wird die [**WM \_ SYSCOMMAND-Nachricht an**](/windows/desktop/menurc/wm-syscommand) das Fenster gesendet.

Im Gegensatz [**zu den \_ WM-Meldungen NCLBUTTONDOWN,**](wm-nclbuttondown.md) [**WM \_ NCMBUTTONDOWN**](wm-ncmbuttondown.md)und [**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md) sollte eine Anwendung **true** aus dieser Nachricht zurückgeben, wenn sie sie verarbeitet. Dies ermöglicht Software, die diese Nachricht auf Windows-Systemen vor Windows 2000 simuliert, um zu bestimmen, ob die Fensterprozedur die Nachricht verarbeitet oder [**DefWindowProc aufgerufen**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) hat, um sie zu verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winuser.h (einschließlich Windowsx.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**WM \_ NCHITTEST**](wm-nchittest.md)
</dt> <dt>

[**WM \_ NCXBUTTONDBLCLK**](wm-ncxbuttondblclk.md)
</dt> <dt>

[**WM \_ NCXBUTTONUP**](wm-ncxbuttonup.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punkte**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

