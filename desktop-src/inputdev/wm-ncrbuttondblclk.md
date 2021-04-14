---
title: WM_NCRBUTTONDBLCLK Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer mit der rechten Maustaste doppelklickt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.
ms.assetid: 20d62b05-07de-49da-b160-29fa1f5067fa
keywords:
- Tastatur-und Maus Eingaben für WM_NCRBUTTONDBLCLK Nachricht
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
ms.openlocfilehash: fee33d9b31f99a00181427c9a715df792d95fe55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518329"
---
# <a name="wm_ncrbuttondblclk-message"></a>WM- \_ ncrbuttondblclk-Meldung

Wird gesendet, wenn der Benutzer mit der rechten Maustaste doppelklickt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_NCRBUTTONDBLCLK              0x00A6
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Treffer Test Wert, der von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion als Ergebnis der Verarbeitung der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht zurückgegeben wird. Eine Liste der Treffer Test Werte finden Sie unter **WM \_ nchittest**.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur, die die x-und y-Koordinaten des Cursors enthält. Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Ein Fenster muss nicht den **CS- \_ dblclks** -Stil aufweisen, um **WM \_ ncrbuttondblclk** -Meldungen zu empfangen.

Das System generiert eine **WM- \_ ncrbuttondblclk** -Meldung, wenn der Benutzer die Maustaste drückt, loslässt und erneut mit der rechten Maustaste im Doppelklick-Zeit Limit des Systems drückt. Durch Doppelklicken auf die Rechte Maustaste werden tatsächlich vier Meldungen generiert [**: \_ WM ncrbuttondown**](wm-ncrbuttondown.md), [**WM \_ ncrbuttonup**](wm-ncrbuttonup.md), **WM \_ ncrbuttondblclk** und **WM \_ ncrbuttonup** .

Sie können auch die Makros [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die Werte der X-und y-Koordinaten aus *LPARAM* zu extrahieren.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.

 

Wenn dies der Fall ist, sendet das System die WM- [**\_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Meldung an das Fenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winuser. h (Include WINDOWSX. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**\_Y- \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**WM- \_ nchittest**](wm-nchittest.md)
</dt> <dt>

[**WM- \_ ncrbuttondown**](wm-ncrbuttondown.md)
</dt> <dt>

[**WM- \_ ncrbuttonup**](wm-ncrbuttonup.md)
</dt> <dt>

[**WM ( \_ syscommand)**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Licher**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punkt**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

