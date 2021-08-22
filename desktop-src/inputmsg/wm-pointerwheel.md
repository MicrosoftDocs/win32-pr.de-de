---
title: WM_POINTERWHEEL-Nachricht
description: Wird im Fenster mit dem Vordergrundtastaturfokus angezeigt, wenn ein Scrollrad gedreht wird.
ms.assetid: 6eec37da-2200-4be1-bf0b-44704caa1320
keywords:
- 'WM_POINTERWHEEL-Nachricht: Eingabemeldungen und Benachrichtigungen'
topic_type:
- apiref
api_name:
- WM_POINTERWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 93144125c21da2d29a0d71f56d8d865da4a07dda6adff2f25ce3528fca72b475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118756528"
---
# <a name="wm_pointerwheel-message"></a>WM_POINTERWHEEL-Nachricht

Wird im Fenster mit dem Vordergrundtastaturfokus angezeigt, wenn ein Scrollrad gedreht wird.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Wichtig\]  
> Desktop-Apps sollten DPI-bewusst sein. Wenn Ihre App keine DPI-Unterstützung hat, können Bildschirmkoordinaten, die in Zeigermeldungen und verwandten Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Writing High-DPI Win32 Applications ( Schreiben von Win32-Anwendungen mit hohem DPI-Code).](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_POINTERWHEEL            0x024E
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält den Zeigerbezeichner und das Raddelta. Verwenden Sie die folgenden Makros, um diese Informationen abzurufen.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Zeigerbezeichner.

[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): Raddelta als kurz signierter Wert.

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält die Punktposition des Zeigers.

> [!Note]  
> Da der Zeiger den Kontakt mit dem Gerät über einen nicht trivialen Bereich stellen kann, kann diese Punktposition eine Vereinfachung eines komplexeren Zeigerbereichs sein. Wenn möglich, sollte eine Anwendung die vollständigen Zeigerbereichsinformationen anstelle der Punktposition verwenden.

 

Verwenden Sie die folgenden Makros, um die physischen Bildschirmkoordinaten des Punkts abzurufen.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): Die x-Koordinate (horizontaler Punkt).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): Die y-Koordinate (vertikaler Punkt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

Wenn die Anwendung diese Meldung nicht verarbeiten kann, sollte sie [**DefWindowProc aufrufen.**](/windows/win32/api/winuser/nf-winuser-defwindowproca)

## <a name="remarks"></a>Hinweise

Um die Scrolleinheiten für das Rad abzurufen, verwenden Sie die **inputData-Datei** der [**POINTER_INFO,die**](/previous-versions/windows/desktop/api) durch Aufrufen der [**GetPointerInfo-Funktion zurückgegeben**](/previous-versions/windows/desktop/api) wird. Dieses Feld enthält einen Wert mit Vorsigniertem und wird in einem Vielfachen von **WHEEL_DELTA.** Ein positiver Wert gibt eine Drehung vorwärts und ein negativer Wert eine Rückwärtsdrehung an.

Beachten Sie, dass die Radeingaben auch dann übermittelt werden können, wenn sich der Mauszeiger außerhalb des Anwendungsfensters befindet. Die Radmeldungen werden auf eine Weise übermittelt, die den Tastatureingaben sehr ähnlich ist. Das Fokusfenster der nachrichtenwarteschlange empfängt die Radnachrichten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Meldungen](messages.md)
</dt> </dl>

 

