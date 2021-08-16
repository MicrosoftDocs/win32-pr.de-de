---
title: WM_NCRBUTTONDBLCLK-Nachricht (Winuser.h)
description: Wird gepostet, wenn der Benutzer mit der rechten Maustaste doppelklickt, während sich der Cursor im Nichtclientbereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gesendet.
ms.assetid: 20d62b05-07de-49da-b160-29fa1f5067fa
keywords:
- WM_NCRBUTTONDBLCLK Meldung Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_NCRBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af62a21da645a265e5264ffae47ad8cb0907ec6fb0106cfb9e7cee97b7f42e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666300"
---
# <a name="wm_ncrbuttondblclk-message"></a>WM \_ NCRBUTTONDBLCLK-Nachricht

Wird gepostet, wenn der Benutzer mit der rechten Maustaste doppelklickt, während sich der Cursor im Nichtclientbereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gesendet.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCRBUTTONDBLCLK              0x00A6
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Von der [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) als Ergebnis der Verarbeitung der [**WM \_ NCHITTEST-Nachricht**](wm-nchittest.md) zurückgegebene Treffertestwert. Eine Liste der Treffertestwerte finden Sie unter **WM \_ NCHITTEST**.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [](/previous-versions//dd162808(v=vs.85)) POINTS-Struktur, die die x- und y-Koordinaten des Cursors enthält. Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Ein Fenster muss nicht den **CS \_ DBLCLKS-Stil** aufweisen, um **WM \_ NCRBUTTONDBLCLK-Nachrichten** zu empfangen.

Das System generiert eine **WM \_ NCRBUTTONDBLCLK-Meldung,** wenn der Benutzer die rechte Maustaste innerhalb des Doppelklick-Zeitlimits des Systems drückt, loslässt und erneut drückt. Wenn Sie mit der rechten Maustaste doppelklicken, werden vier Meldungen generiert: [**WM \_ NCRBUTTONDOWN,**](wm-ncrbuttondown.md) [**WM \_ NCRBUTTONUP,**](wm-ncrbuttonup.md) **WM \_ NCRBUTTONDBLCLK** und **WM \_ NCRBUTTONUP.**

Sie können auch die [**Makros GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die Werte der x- und y-Koordinaten aus *lParam* zu extrahieren.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Verwenden Sie nicht die [**LOWORD-**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) oder [**HIWORD-Makros,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) um die x- und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse auf Systemen mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können negative x- und y-Koordinaten aufweisen, und **LOWORD** und **HIWORD** behandeln die Koordinaten als Mengen ohne Vorzeichen.

 

Wenn dies sinnvoll ist, sendet das System die [**\_ WM-SYSCOMMAND-Nachricht**](/windows/desktop/menurc/wm-syscommand) an das Fenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winuser.h (windowsx.h einschließen)</dt> </dl> |



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

[**WM \_ NCRBUTTONDOWN**](wm-ncrbuttondown.md)
</dt> <dt>

[**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md)
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

 

