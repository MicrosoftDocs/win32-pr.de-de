---
title: WM_NCMBUTTONDBLCLK (Winuser.h)
description: Wird veröffentlicht, wenn der Benutzer auf die mittlere Maustaste doppelklickt, während sich der Cursor im Nicht-Clientbereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gesendet.
ms.assetid: 7c0f8d6e-eb37-4873-a3f8-777e8b0b22bc
keywords:
- WM_NCMBUTTONDBLCLK der Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_NCMBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf5c963dac002c74e49d2d112979b23ce10e1205cafa3653b82fb1a0703c863
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778460"
---
# <a name="wm_ncmbuttondblclk-message"></a>WM \_ NCMBUTTONDBLCLK-Meldung

Wird veröffentlicht, wenn der Benutzer auf die mittlere Maustaste doppelklickt, während sich der Cursor im Nicht-Clientbereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gesendet.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCMBUTTONDBLCLK              0x00A9
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

Ein Fenster muss nicht über das **CS \_ DBLCLKS-Format** verfügen, um **WM \_ NCMBUTTONDBLCLK-Nachrichten zu** empfangen.

Das System generiert eine **WM \_ NCMBUTTONDBLCLK-Meldung,** wenn der Benutzer die mittlere Maustaste innerhalb des Zeitlimits für Doppelklicks drückt, loslässt und erneut drückt. Durch Doppelklicken auf die mittlere Maustaste werden tatsächlich vier Meldungen generiert: [**WM \_ NCMBUTTONDOWN,**](wm-ncmbuttondown.md) [**WM \_ NCMBUTTONUP,**](wm-ncmbuttonup.md) **WM \_ NCMBUTTONDBLCLK** und **WM \_ NCMBUTTONUP.**

Sie können auch die [**GET \_ X \_ LPARAM-**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**GET \_ \_ Y-LPARAM-Makros**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die Werte der x- und y-Koordinaten aus *lParam zu extrahieren.*


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Verwenden Sie nicht die [**LOWORD-**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) oder [**HIWORD-Makros,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) um die x- und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse auf Systemen mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können negative x- und y-Koordinaten haben, **und LOWORD** und **HIWORD** behandeln die Koordinaten als Mengen ohne Vorzeichen.

 

Wenn dies sinnvoll ist, sendet das System die [**WM \_ SYSCOMMAND-Nachricht**](/windows/desktop/menurc/wm-syscommand) an das Fenster.

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

[**WM \_ NCMBUTTONDOWN**](wm-ncmbuttondown.md)
</dt> <dt>

[**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md)
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

 

