---
title: WM_NCXBUTTONUP-Nachricht (Winuser.h)
description: Wird gesendet, wenn der Benutzer die erste oder zweite X-Schaltfläche freigibt, während sich der Cursor im Nichtclientbereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gesendet.
ms.assetid: 07ab5d4e-9912-4867-9146-8abc5addc15d
keywords:
- WM_NCXBUTTONUP Meldung Tastatur- und Mauseingabe
topic_type:
- apiref
api_name:
- WM_NCXBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eab2067d3d16c3ae0864ba7ddf04b5666efa0186d0a7d55ebd5eddaa7533790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829900"
---
# <a name="wm_ncxbuttonup-message"></a>WM \_ NCXBUTTONUP-Meldung

Wird gesendet, wenn der Benutzer die erste oder zweite X-Schaltfläche freigibt, während sich der Cursor im Nichtclientbereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung *nicht* gesendet.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCXBUTTONUP                  0x00AC
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt den Treffertestwert an, der von der [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) bei der Verarbeitung der [**\_ WM-NCHITTEST-Nachricht**](wm-nchittest.md) zurückgegeben wird. Eine Liste der Treffertestwerte finden Sie unter **WM \_ NCHITTEST**.

Das Wort in hoher Reihenfolge gibt an, welche Schaltfläche losgelassen wurde. Dieses Argument einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                     | Bedeutung                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1-0x0001**</dt> <dt></dt> </dl> | Die erste X-Schaltfläche wurde freigegeben.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2-0x0002**</dt> <dt></dt> </dl> | Die zweite X-Schaltfläche wurde freigegeben.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger [](/previous-versions//dd162808(v=vs.85)) auf eine POINTS-Struktur, die die x- und y-Koordinaten des Cursors enthält. Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie **TRUE** zurückgeben. Weitere Informationen zur Verarbeitung des Rückgabewerts finden Sie im Abschnitt Hinweise.

## <a name="remarks"></a>Hinweise

Verwenden Sie den folgenden Code, um die Informationen im *wParam-Parameter* abzurufen.


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



Sie können auch den folgenden Code verwenden, um die x- und y-Koordinaten von *lParam* abzurufen:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Verwenden Sie nicht die [**LOWORD-**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) oder [**HIWORD-Makros,**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) um die x- und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse auf Systemen mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können negative x- und y-Koordinaten aufweisen, und **LOWORD** und **HIWORD** behandeln die Koordinaten als Mengen ohne Vorzeichen.

 

Standardmäßig testet die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) den angegebenen Punkt, um die Position des Cursors abzurufen, und führt die entsprechende Aktion aus. Bei Bedarf wird die [**\_ WM-SYSCOMMAND-Nachricht**](/windows/desktop/menurc/wm-syscommand) an das Fenster gesendet.

Im Gegensatz zu den [**\_ WM-Meldungen NCLBUTTONUP,**](wm-nclbuttonup.md) [**WM \_ NCMBUTTONUP**](wm-ncmbuttonup.md)und [**WM \_ NCRBUTTONUP**](wm-ncrbuttonup.md) sollte eine Anwendung **TRUE** von dieser Nachricht zurückgeben, wenn sie sie verarbeitet. Auf diese Weise kann Software, die diese Nachricht auf Windows Systemen vor Windows 2000 simuliert, bestimmen, ob die Fensterprozedur die Nachricht verarbeitet oder [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aufgerufen hat, um sie zu verarbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winuser.h (windowsx.h einschließen)</dt> </dl> |



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

[**WM \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md)
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

 

