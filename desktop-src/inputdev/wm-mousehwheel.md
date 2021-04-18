---
title: WM_MOUSEHWHEEL Meldung (Winuser. h)
description: Wird an das aktive Fenster gesendet, wenn das horizontale Mausrad der Maus gekippt oder gedreht wird.
ms.assetid: 4d6a3d73-38ef-450d-89d2-2d381fc7a7c3
keywords:
- Tastatur-und Maus Eingaben für WM_MOUSEHWHEEL Nachricht
topic_type:
- apiref
api_name:
- WM_MOUSEHWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1f3b1690ad39919e2a62b50ba6eacec8348e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338138"
---
# <a name="wm_mousehwheel-message"></a>WM- \_ mousehwheel-Meldung

Wird an das aktive Fenster gesendet, wenn das horizontale Mausrad der Maus gekippt oder gedreht wird. Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt die Nachricht an das übergeordnete Fenster des Fensters weiter. Es sollte keine interne Weiterleitung der Nachricht vorhanden sein, da **defwindowproc** Sie in der übergeordneten Kette weitergibt, bis ein Fenster gefunden wird, in dem Sie verarbeitet wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_MOUSEHWHEEL                  0x020E
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das höchst wertige Wort gibt die Entfernung an, um die das Rad gedreht wird, ausgedrückt in Vielfachen oder Faktoren des **\_ raddeltas**, das auf 120 festgelegt ist. Ein positiver Wert gibt an, dass das Mausrad nach rechts gedreht wurde. ein negativer Wert gibt an, dass das Rad nach links gedreht wurde.

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

Verwenden Sie den folgenden Code, um die Informationen im *wParam* -Parameter zu erhalten.


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



Verwenden Sie den folgenden Code, um die horizontale und vertikale Position abzurufen.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Wie bereits erwähnt, befindet sich die x-Koordinate in der unteren **Reihenfolge** des Rückgabewerts. die y-Koordinate befindet sich in der hohen Reihenfolge ( **kurz** ) (beide stellen *signierte* Werte dar, da Sie negative Werte für Systeme mit mehreren Monitoren annehmen können). Wenn der Rückgabewert einer Variablen zugewiesen ist, können Sie mit dem [**makepoints**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) -Makro eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur aus dem Rückgabewert abrufen. Sie können auch das [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) -oder [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) -Makro verwenden, um die X-oder y-Koordinate zu extrahieren.

> [!IMPORTANT]
> Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben. Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.

 

Die Raddrehung ist ein Vielfaches von **\_ raddelta**, das auf 120 festgelegt ist. Dies ist der Schwellenwert für die auszuführende Aktion, und eine Aktion (z. b. durch Scrollen eines Inkrements) sollte für jedes Delta stattfinden.

Das Delta wurde auf 120 festgelegt, um es Microsoft oder anderen Anbietern zu ermöglichen, feinere Auflösungs Räder (z. b. ein rotiertes Rad ohne Notches) zu erstellen, um mehr Nachrichten pro Drehung zu senden, aber mit einem geringeren Wert in jeder Nachricht. Um dieses Feature verwenden zu können, können Sie die eingehenden Delta Werte hinzufügen, bis das **\_ raddelta** erreicht ist (also bei einer Delta Drehung dieselbe Antwort), oder wenn Sie Teil Zeilen als Reaktion auf häufigere Nachrichten scrollen. Sie können auch die Bildlauf-Granularität auswählen und die Delta-Optionen ansammeln, bis Sie erreicht ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
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

 

