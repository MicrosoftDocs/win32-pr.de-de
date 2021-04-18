---
title: WM_NCXBUTTONDBLCLK Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf die erste oder zweite X-Schaltfläche doppelklickt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.
ms.assetid: 8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef
keywords:
- Tastatur-und Maus Eingaben für WM_NCXBUTTONDBLCLK Nachricht
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
ms.openlocfilehash: 1455f6d6c2fa40f34bbfbe00e0c7a30daa52f375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344496"
---
# <a name="wm_ncxbuttondblclk-message"></a>WM- \_ ncxbuttondblclk-Meldung

Wird gesendet, wenn der Benutzer auf die erste oder zweite X-Schaltfläche doppelklickt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_NCXBUTTONDBLCLK              0x00AD
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das nieder wertige Wort gibt den Treffer Testwert an, der von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion aus der Verarbeitung der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht zurückgegeben wird. Eine Liste der Treffer Test Werte finden Sie unter **WM \_ nchittest**.

Das höchst wertige Wort gibt an, auf welche Schaltfläche Doppel geklickt wurde. Dieses Argument einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                     | Bedeutung                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XButton1**</dt> <dt>0x0001</dt> </dl> | Auf die erste X-Schaltfläche wurde Doppel geklickt.<br/> |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XButton2**</dt> <dt>0x0002</dt> </dl> | Auf die zweite X-Schaltfläche wurde Doppel geklickt.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur, die die x-und y-Koordinaten des Cursors enthält. Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben. Weitere Informationen zum Verarbeiten des Rückgabewerts finden Sie im Abschnitt "Hinweise".

## <a name="remarks"></a>Bemerkungen

Verwenden Sie den folgenden Code, um die Informationen im *wParam* -Parameter zu erhalten.


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



Sie können auch den folgenden Code verwenden, um die x-und y-Koordinaten von *LPARAM* zu erhalten:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.

 

Standardmäßig testet die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion den angegebenen Punkt, um die Position des Cursors abzurufen, und führt die entsprechende Aktion aus. Bei Bedarf wird die WM- [**\_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Nachricht an das Fenster gesendet.

Ein Fenster muss nicht den **CS- \_ dblclks** -Stil aufweisen, um die **WM- \_ ncxbuttondblclk** -Meldungen zu empfangen. Das System generiert eine **WM \_ ncxbuttondblclk** -Meldung, wenn der Benutzer eine X-Schaltfläche im Doppelklick-Zeit Limit des Systems drückt, loslässt und erneut drückt. Durch Doppelklicken auf eine dieser Schaltflächen werden tatsächlich vier Meldungen generiert: [**WM \_ ncxbuttondown**](wm-ncxbuttondown.md), [**WM \_ ncxbuttonup**](wm-ncxbuttonup.md), **WM \_ ncxbuttondblclk** und **WM \_ ncxbuttonup** .

Im Gegensatz zu den Nachrichten " [**WM \_ nclbuttondblclk**](wm-nclbuttondblclk.md)", " [**WM \_ ncmbuttondblclk**](wm-ncmbuttondblclk.md)" und "WM [**\_ ncrbuttondblclk**](wm-ncrbuttondblclk.md) " sollte eine Anwendung aus dieser Nachricht " **true** " zurückgeben, wenn Sie sie verarbeitet. Auf diese Weise kann Software, die diese Meldung auf Windows-Systemen vor Windows 2000 simuliert, ermitteln, ob die Fenster Prozedur die Nachricht verarbeitet hat oder [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aufgerufen hat, um Sie zu verarbeiten.

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

[**WM- \_ ncxbuttondown**](wm-ncxbuttondown.md)
</dt> <dt>

[**WM- \_ ncxbuttonup**](wm-ncxbuttonup.md)
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

 

