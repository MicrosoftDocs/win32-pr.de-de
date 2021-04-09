---
title: WM_TOUCHHITTESTING Meldung
description: Wird an ein Fenster in einem Touchscreen gesendet, um das wahrscheinlichste Berührungs Ziel zu ermitteln.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_TOUCHHITTESTING Nachricht
topic_type:
- apiref
api_name:
- WM_TOUCHHITTESTING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 83b6e564d692fb0223ec8871b99cefcb9fddf40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104558"
---
# <a name="wm_touchhittesting-message"></a>WM_TOUCHHITTESTING Meldung

Wird an ein Fenster in einem Touchscreen gesendet, um das wahrscheinlichste Berührungs Ziel zu ermitteln.

> \[! Wichtig\]  
> Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_TOUCHHITTESTING       0x024D
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) Struktur, die die Daten des Berührungs Kontakt Bereichs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn sich ein oder mehrere Elemente im Touch-Kontaktbereich befinden, sollte eine Anwendung das Ergebnis von [**packtouchhittestingproximityevaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)zurückgeben.

Wenn sich keine Elemente im Touch-Kontaktbereich befinden, sollte eine Anwendung den Wert von **Score** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) auf [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) festlegen und [**packtouchhittestingproximityevaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) aufrufen, um den LRESULT-Rückgabewert zu erhalten.

Wenn die Anwendung diese Nachricht nicht verarbeitet, muss Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird an Windows gesendet, die über die [**registertouchhittestingwindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) -Funktion registriert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> <dt>

[**Treffer Treffer Test-Ergebnisse**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

