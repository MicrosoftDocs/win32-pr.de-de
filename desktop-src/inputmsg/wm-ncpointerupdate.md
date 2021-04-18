---
title: WM_NCPOINTERUPDATE Meldung
description: Wird bereitgestellt, um ein Update für einen Zeiger bereitzustellen, der den Kontakt über den nicht-Client Bereich eines Fensters hergestellt hat, oder wenn ein nicht erfasster Kontakt, der sich im nicht-Client Bereich eines Fensters bewegt, verschoben wird
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704caa1322
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_NCPOINTERUPDATE Nachricht
topic_type:
- apiref
api_name:
- WM_NCPOINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 09ef5fd6f3b7378a963be4278f1fabdf0f6ab351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391789"
---
# <a name="wm_ncpointerupdate-message"></a>WM_NCPOINTERUPDATE Meldung

Wird bereitgestellt, um ein Update für einen Zeiger bereitzustellen, der den Kontakt über den nicht-Client Bereich eines Fensters hergestellt hat, oder wenn ein nicht erfasster Kontakt, der sich im nicht-Client Bereich eines Fensters bewegt, verschoben wird Während der Mauszeiger bewegt wird, wird die Nachricht auf das Fenster ausgerichtet, über das sich der Zeiger befindet. Während sich der Mauszeiger auf der-Oberfläche befindet, wird der Zeiger implizit in dem Fenster erfasst, über das der Zeiger den Kontakt hergestellt hat, und dieses Fenster empfängt weiterhin Eingaben für den Zeiger, bis der Kontakt unterbrochen wird.

Wenn ein Fenster diesen Zeiger aufgezeichnet hat, wird diese Meldung nicht gepostet. Stattdessen wird ein [**WM_POINTERUPDATE**](wm-pointerupdate.md) an das Fenster gesendet, das diesen Zeiger aufgezeichnet hat.

> \[! Wichtig\]  
> Desktop-Apps sollten dpi-fähig sein. Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen. Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_NCPOINTERUPDATE                 0x0241
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält den Zeiger Bezeichner und zusätzliche Informationen. Verwenden Sie die folgenden Makros, um diese Informationen abzurufen.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Zeiger Bezeichner

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): Treffer Test Wert, der von der Verarbeitung der [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) Nachricht zurückgegeben wurde.

</dd> <dt>

*lParam* 
</dt> <dd>

Enthält die Punktposition des Zeigers.

> [!Note]  
> Da der Zeiger über einen nicht trivialen Bereich eine Verbindung mit dem Gerät herstellen kann, kann es sein, dass diese Punktposition eine Vereinfachung eines komplexeren Zeiger Bereichs ist. Wenn möglich, sollte eine Anwendung anstelle der Punktposition die gesamten Zeiger Bereichs Informationen verwenden.

 

Verwenden Sie die folgenden Makros zum Abrufen der physischen Bildschirm Koordinaten des Punkts.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(LPARAM): die X-Koordinate (horizontal Punkt).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(LPARAM): die Y-Koordinate (vertikal Punkt).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.

## <a name="remarks"></a>Bemerkungen

Wenn die Anwendung diese Nachricht nicht verarbeitet, kann [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) eine oder mehrere System Aktionen ausführen, je nachdem, welches Treffer Testergebnis in der Nachricht enthalten ist. In der Regel sollten Anwendungen diese Nachricht nicht verarbeiten müssen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Meldungen](messages.md)
</dt> </dl>

 

