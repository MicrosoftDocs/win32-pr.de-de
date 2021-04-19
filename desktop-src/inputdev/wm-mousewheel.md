---
title: WM_MOUSEWHEEL Meldung (Winuser. h)
description: Wird an das Fokus Fenster gesendet, wenn das Mausrad gedreht wird.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- Tastatur-und Maus Eingaben für WM_MOUSEWHEEL Nachricht
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b918989b41b43c3f54d8ec3133223716e839e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338724"
---
# <a name="wm_mousewheel-message"></a>WM- \_ mouswheel-Meldung

Wird an das Fokus Fenster gesendet, wenn das Mausrad gedreht wird. Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt die Nachricht an das übergeordnete Fenster des Fensters weiter. Es sollte keine interne Weiterleitung der Nachricht vorhanden sein, da **defwindowproc** Sie in der übergeordneten Kette weitergibt, bis ein Fenster gefunden wird, in dem Sie verarbeitet wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das höchst wertige Wort gibt die Entfernung an, um die das Rad gedreht wird, ausgedrückt in Vielfachen oder Abteilungen des **\_ raddeltas**, das 120 ist. Ein positiver Wert gibt an, dass das Rad vom Benutzer entfernt wurde. ein negativer Wert gibt an, dass das Rad in Richtung des Benutzers rückwärts gedreht wurde.

Das nieder wertige Wort gibt an, ob verschiedene virtuelle Schlüssel ausfallen. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                               | Bedeutung                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Steuer**</dt> Element <dt>0x0008</dt> </dl>    | Die STRG-Taste ist nicht gedrückt.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ Lbutton**</dt> <dt>0x0001</dt> </dl>    | Die linke Maustaste ist nicht mehr vorhanden.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MButton**</dt> <dt>0x0010</dt> </dl>    | Die mittlere Maustaste ist nicht mehr angezeigt.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ Rbutton**</dt> <dt>0x0002</dt> </dl>    | Die Rechte Maustaste ist nicht mehr angezeigt.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ UMSCHALT**</dt> <dt>0x0004</dt> </dl>          | Die UMSCHALTTASTE ist nicht mehr festgelegt.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XButton1**</dt> <dt>0x0020</dt> </dl> | Die erste X-Schaltfläche ist nicht angezeigt.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XButton2**</dt> <dt>0x0040</dt> </dl> | Die zweite X-Schaltfläche ist nicht mehr festgelegt.<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort gibt die x-Koordinate des Zeigers relativ zur oberen linken Ecke des Bildschirms an.

Das höchst wertige Wort gibt die y-Koordinate des Zeigers relativ zur oberen linken Ecke des Bildschirms an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie den folgenden Code, um die Informationen im *wParam* -Parameter zu erhalten:


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Verwenden Sie den folgenden Code zum Abrufen der horizontalen und vertikalen Position:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Wie bereits erwähnt, befindet sich die x-Koordinate in der unteren **Reihenfolge** des Rückgabewerts. die y-Koordinate befindet sich in der hohen Reihenfolge ( **kurz** ) (beide stellen *signierte* Werte dar, da Sie negative Werte für Systeme mit mehreren Monitoren annehmen können). Wenn der Rückgabewert einer Variablen zugewiesen ist, können Sie mit dem [**makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) -Makro eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur aus dem Rückgabewert abrufen. Sie können auch das [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) -oder [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) -Makro verwenden, um die X-oder y-Koordinate zu extrahieren.

> [!IMPORTANT]
> Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.

 

Die Raddrehung ist ein Vielfaches von **\_ raddelta**, das bei 120 festgelegt wird. Dies ist der Schwellenwert für die auszuführende Aktion, und eine Aktion (z. b. durch Scrollen eines Inkrements) sollte für jedes Delta stattfinden.

Das Delta wurde auf 120 festgelegt, um es Microsoft oder anderen Anbietern zu ermöglichen, feinere Auflösungs Räder (ein rotiertes Rad ohne Notches) zu erstellen, um mehr Nachrichten pro Drehung zu senden, aber mit einem geringeren Wert in jeder Nachricht. Um dieses Feature verwenden zu können, können Sie die eingehenden Delta Werte hinzufügen, bis das **\_ raddelta** erreicht ist (sodass Sie für eine Delta Drehung dieselbe Antwort erhalten), oder indem Sie Teil Zeilen als Reaktion auf häufigere Nachrichten scrollen. Sie können auch die Bildlauf-Granularität auswählen und die Delta-Optionen ansammeln, bis Sie erreicht ist.

Beachten Sie, dass es keine *Schlüssel* für das **msh- \_ mouswheel** gibt. Andernfalls sind die Parameter genau identisch mit denen für **WM \_ mouswheel**.

Die Anwendung kann **msh \_ MouseWheel** an alle eingebetteten Objekte oder Steuerelemente weiterleiten. Die Anwendung ist erforderlich, um die Nachricht an eine aktive eingebettete OLE-Anwendung zu senden. Es ist optional, dass die Anwendung diese an ein Rad aktiviertes Steuerelement mit dem Fokus sendet. Wenn die Anwendung die Nachricht an ein Steuerelement sendet, kann Sie den Rückgabewert überprüfen, um festzustellen, ob die Nachricht verarbeitet wurde. Steuerelemente müssen den Wert " **true** " zurückgeben, wenn Sie die Nachricht verarbeiten.

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

[**\_KeyState- \_ wParam-Element**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**\_Y- \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**\_ \_ rasterdelta- \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**Maus \_ Ereignis**](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

**Licher**
</dt> <dt>

[Mauseingabe](mouse-input.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[**Makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punkt**](/previous-versions//dd162808(v=vs.85))
</dt> <dt>

[**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

