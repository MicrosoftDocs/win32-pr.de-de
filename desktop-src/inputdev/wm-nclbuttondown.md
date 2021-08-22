---
title: WM_NCLBUTTONDOWN (Winuser.h)
description: Wird gepostet, wenn der Benutzer die linke Maustaste drückt, während sich der Cursor im Nicht-Clientbereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gesendet.
ms.assetid: fca6d9ec-c549-4c82-9a80-15471481f876
keywords:
- WM_NCLBUTTONDOWN der Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_NCLBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a99be93ab695429ce7475fe555ce6d40ae84e7435190809cb10dffa58ade10c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778550"
---
# <a name="wm_nclbuttondown-message"></a>WM \_ NCLBUTTONDOWN-Meldung

Wird gepostet, wenn der Benutzer die linke Maustaste drückt, während sich der Cursor im Nicht-Clientbereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gesendet.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCLBUTTONDOWN                0x00A1
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Treffertestwert, der von der [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) als Ergebnis der Verarbeitung der [**WM \_ NCHITTEST-Nachricht zurückgegeben**](wm-nchittest.md) wird. Eine Liste der Treffertestwerte finden Sie unter **WM \_ NCHITTEST**.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [](/previous-versions//dd162808(v=vs.85)) POINTS-Struktur, die die x- und y-Koordinaten des Cursors enthält. Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) testet den angegebenen Punkt, um die Position des Cursors zu finden, und führt die entsprechende Aktion aus. Gegebenenfalls sendet **DefWindowProc** die [**WM \_ SYSCOMMAND-Nachricht**](/windows/desktop/menurc/wm-syscommand) an das Fenster.

Sie können auch die [**GET \_ X \_ LPARAM-**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**GET \_ \_ Y-LPARAM-Makros**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die Werte der x- und y-Koordinaten aus *lParam zu extrahieren.*


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Verwenden Sie nicht die [**LOWORD-**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) oder [**HIWORD-Makros,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) um die x- und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse auf Systemen mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können negative x- und y-Koordinaten haben, **und LOWORD** und **HIWORD** behandeln die Koordinaten als Mengen ohne Vorzeichen.

 

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

[**WM \_ NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md)
</dt> <dt>

[**WM \_ NCLBUTTONUP**](wm-nclbuttonup.md)
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

 

