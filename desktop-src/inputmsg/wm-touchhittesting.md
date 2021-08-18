---
title: WM_TOUCHHITTESTING Meldung
description: Wird in einem Touch-Down an ein Fenster gesendet, um das wahrscheinlichste Touchziel zu ermitteln.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- WM_TOUCHHITTESTING von Nachrichteneingabenachrichten und -benachrichtigungen
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
ms.openlocfilehash: 895c535330674767683d0155bd2e22b8a40389c08378187377497380d71d97b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829490"
---
# <a name="wm_touchhittesting-message"></a>WM_TOUCHHITTESTING Meldung

Wird in einem Touch-Down an ein Fenster gesendet, um das wahrscheinlichste Touchziel zu ermitteln.

> \[! Wichtig\]  
> Desktop-Apps sollten DPI-fähige Apps sein. Wenn Ihre App nicht DPI-bewusst ist, können Bildschirmkoordinaten, die in Zeigermeldungen und zugehörigen Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von Win32-Anwendungen mit hohem DPI-Anteil.](/previous-versions//dd464660(v=vs.85))

 


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

Zeiger auf die [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) Struktur, die die Touchkontaktbereichsdaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn sich mindestens ein Element innerhalb des Berührungskontaktbereichs befindet, sollte eine Anwendung das Ergebnis von [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)zurückgeben.

Wenn sich keine Elemente im Berührungskontaktbereich befinden, sollte eine Anwendung den Wert der **Bewertung** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) auf [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) festlegen und [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) aufrufen, um den LRESULT-Rückgabewert abzurufen.

Wenn die Anwendung diese Nachricht nicht verarbeitet, muss [**sie DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufrufen.

## <a name="remarks"></a>Hinweise

Diese Meldung wird an Fenster gesendet, die sich über die [**RegisterTouchHitTestingWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) registrieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meldungen](messages.md)
</dt> <dt>

[**Treffertestergebnisse für Toucheingaben**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

