---
title: WM_NCPOINTERDOWN-Nachricht
description: Wird gepostet, wenn ein Zeiger den Kontakt über den nicht clientseitigen Bereich eines Fensters vor stellt.
ms.assetid: 3bdc37da-217c-4be1-bf0b-99704bda1322
keywords:
- WM_NCPOINTERDOWN von Nachrichteneingabemeldungen und -benachrichtigungen
topic_type:
- apiref
api_name:
- WM_NCPOINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 419af1c613c979d30f479fc0739cd82f01b538f9ff4d3caa63839af8a40b0caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036058"
---
# <a name="wm_ncpointerdown-message"></a>WM_NCPOINTERDOWN-Nachricht

Wird gepostet, wenn ein Zeiger den Kontakt über den nicht clientseitigen Bereich eines Fensters vor stellt. Die Nachricht ist auf das Fenster festgelegt, über das der Zeiger kontakt mit ihr kontaktt. Der Zeiger wird implizit auf das Fenster erfasst, sodass das Fenster weiterhin Eingaben für den Zeiger erhält, bis er den Kontakt unterbricht.

Wenn ein Fenster diesen Zeiger erfasst hat, wird diese Meldung nicht gesendet. Stattdessen wird [**ein WM_POINTERDOWN**](wm-pointerdown.md) an das Fenster gesendet, das diesen Zeiger erfasst hat.

> \[! Wichtig\]  
> Desktop-Apps sollten DPI-bewusst sein. Wenn Ihre App keine DPI-Unterstützung hat, können Bildschirmkoordinaten, die in Zeigermeldungen und verwandten Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Writing High-DPI Win32 Applications ( Schreiben von Win32-Anwendungen mit hohem DPI-Code).](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_NCPOINTERDOWN                 0x0242
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält den Zeigerbezeichner und zusätzliche Informationen. Verwenden Sie die folgenden Makros, um diese Informationen abzurufen.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Zeigerbezeichner.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): Treffertestwert, der von der Verarbeitung der WM_NCHITTEST [**zurückgegeben**](../inputdev/wm-nchittest.md) wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält die Punktposition des Zeigers.

> [!Note]  
> Da der Zeiger den Kontakt mit dem Gerät über einen nicht trivialen Bereich stellen kann, kann diese Punktposition eine Vereinfachung eines komplexeren Zeigerbereichs sein. Wenn möglich, sollte eine Anwendung die vollständigen Zeigerbereichsinformationen anstelle der Punktposition verwenden.

 

Verwenden Sie die folgenden Makros, um die physischen Bildschirmkoordinaten des Punkts abzurufen.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): Die x-Koordinate (horizontaler Punkt).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): die y-Koordinate (vertikaler Punkt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

Wenn die Anwendung diese Nachricht nicht verarbeiten kann, sollte sie [**DefWindowProc aufrufen.**](/windows/win32/api/winuser/nf-winuser-defwindowproca)

## <a name="remarks"></a>Hinweise

Wenn die Anwendung diese Nachricht nicht verarbeiten kann, kann [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) je nach treffertestbasiertem Ergebnis, das in der Nachricht enthalten ist, eine oder mehrere Systemaktionen ausführen. In der Regel sollten Anwendungen diese Meldung nicht verarbeiten müssen.

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

 

