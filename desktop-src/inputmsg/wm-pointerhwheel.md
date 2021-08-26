---
title: WM_POINTERHWHEEL Meldung
description: Wird an das Fenster mit Vordergrundtastenfokus gesendet, wenn ein horizontales Scrollrad gedreht wird.
ms.assetid: 6eec37da-2200-4be1-bf0b-44504caa1320
keywords:
- WM_POINTERHWHEEL Der Nachrichteneingabenachrichten und -benachrichtigungen
topic_type:
- apiref
api_name:
- WM_NCPOINTERCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9de03b198603f06b4c1c1401714bd2fd5edfe28784890c4b9ab00a025dbaab7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015233"
---
# <a name="wm_pointerhwheel-message"></a>WM_POINTERHWHEEL Meldung

Wird an das Fenster mit Vordergrundtastenfokus gesendet, wenn ein horizontales Scrollrad gedreht wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Wichtig\]  
> Desktop-Apps sollten DPI-fähige Apps sein. Wenn Ihre App nicht DPI-bewusst ist, können Bildschirmkoordinaten, die in Zeigermeldungen und zugehörigen Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von Win32-Anwendungen mit hohem DPI-Anteil.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERHWHEEL            0x024F
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält den Zeigerbezeichner und das Raddelta. Verwenden Sie die folgenden Makros, um diese Informationen abzurufen.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Zeigerbezeichner.

[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): Raddelta als Kurzwert mit Vorzeichen.

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält die Punktposition des Zeigers.

> [!Note]  
> Da der Zeiger den Kontakt mit dem Gerät über einen nicht trivialen Bereich herstellen kann, kann diese Punktposition eine Vereinfachung eines komplexeren Zeigerbereichs sein. Wenn möglich, sollte eine Anwendung anstelle der Punktposition die vollständigen Zeigerbereichsinformationen verwenden.

 

Verwenden Sie die folgenden Makros, um die physischen Bildschirmkoordinaten des Punkts abzurufen.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): die x-Koordinate (horizontaler Punkt).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): die y-Koordinate (vertikaler Punkt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte sie [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufrufen.

## <a name="remarks"></a>Hinweise

Um die Scrolleinheiten des Rads abzurufen, verwenden Sie den **InputData-Eintrag** der [**POINTER_INFO**](/previous-versions/windows/desktop/api) Struktur, die durch Aufrufen der [**GetPointerInfo-Funktion**](/previous-versions/windows/desktop/api) zurückgegeben wird. Dieses Feld enthält einen Wert mit Vorzeichen und wird in einem Vielfachen von **WHEEL_DELTA** ausgedrückt. Ein positiver Wert gibt eine Drehung nach vorn und ein negativer Wert eine Drehung rückwärts an.

Beachten Sie, dass die Radeingaben auch dann übermittelt werden können, wenn sich der Mauszeiger außerhalb des Fensters der Anwendung befindet. Die Wheelnachrichten werden ähnlich wie die Tastatureingaben übermittelt. Das Fokusfenster der vorhergehenden Nachrichtenwarteschlange empfängt die Wheelnachrichten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> </dl>

 

