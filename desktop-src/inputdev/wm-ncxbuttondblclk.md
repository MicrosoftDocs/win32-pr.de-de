---
title: WM_NCXBUTTONDBLCLK (Winuser.h)
description: Wird veröffentlicht, wenn der Benutzer auf die erste oder zweite X-Schaltfläche doppelklickt, während sich der Cursor im Nicht-Clientbereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gesendet.
ms.assetid: 8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef
keywords:
- WM_NCXBUTTONDBLCLK der Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b5b0deb3efb84af2bdd862377411d86328ee7ef72242a6e27759b819cdab2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482640"
---
# <a name="wm_ncxbuttondblclk-message"></a>WM \_ NCXBUTTONDBLCLK-Meldung

Wird veröffentlicht, wenn der Benutzer auf die erste oder zweite X-Schaltfläche doppelklickt, während sich der Cursor im Nicht-Clientbereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gesendet.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCXBUTTONDBLCLK              0x00AD
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Wort in niedriger Reihenfolge gibt den Treffertestwert an, der von der [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) bei der Verarbeitung der [**WM \_ NCHITTEST-Nachricht zurückgegeben**](wm-nchittest.md) wird. Eine Liste der Treffertestwerte finden Sie unter **WM \_ NCHITTEST**.

Das obere Wort gibt an, auf welche Schaltfläche doppelklickt wurde. Dieses Argument einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                     | Bedeutung                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1-0x0001**</dt> <dt></dt> </dl> | Auf die erste X-Schaltfläche wurde doppelklicken.<br/> |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2-0x0002**</dt> <dt></dt> </dl> | Auf die zweite X-Schaltfläche wurde doppelklicken.<br/> |



 

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

Ein Fenster muss nicht über das **CS \_ DBLCLKS-Format** verfügen, um **WM \_ NCXBUTTONDBLCLK-Nachrichten zu** empfangen. Das System generiert eine **WM \_ NCXBUTTONDBLCLK-Meldung,** wenn der Benutzer eine X-Taste innerhalb des Zeitlimits für Doppelklicken des Systems drückt, loslässt und erneut drückt. Wenn Sie auf eine dieser Schaltflächen doppelklicken, werden tatsächlich vier Meldungen generiert: [**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md), [**WM \_ NCXBUTTONUP,**](wm-ncxbuttonup.md) **WM \_ NCXBUTTONDBLCLK** und **WM \_ NCXBUTTONUP.**

Im Gegensatz [**zu den \_ WM-Meldungen NCLBUTTONDBLCLK,**](wm-nclbuttondblclk.md) [**WM \_ NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md)und [**WM \_ NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) sollte eine Anwendung **true** aus dieser Meldung zurückgeben, wenn sie sie verarbeitet. Auf diese Weise kann Software, die diese Nachricht auf Windows-Systemen vor Windows 2000 simuliert, bestimmen, ob die Fensterprozedur die Nachricht verarbeitet oder [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aufgerufen hat, um sie zu verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winuser.h (einschließlich Windowsx.h)</dt> </dl> |



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

[**WM \_ NCHITTEST**](wm-nchittest.md)
</dt> <dt>

[**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md)
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

 

