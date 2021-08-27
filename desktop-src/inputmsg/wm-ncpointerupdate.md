---
title: WM_NCPOINTERUPDATE Meldung
description: Wird veröffentlicht, um ein Update für einen Zeiger bereitzustellen, der den Kontakt über den Nicht-Clientbereich eines Fensters hergestellt hat oder wenn ein nicht gekapselter Kontakt mit dem Mauszeiger über den Nicht-Clientbereich eines Fensters bewegt wird.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_NCPOINTERUPDATE Nachrichteneingabenachrichten und -benachrichtigungen
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
ms.openlocfilehash: 6f1cf786af00175f75b5faee11b384aa31618d89427826f9c1454006df461f0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062420"
---
# <a name="wm_ncpointerupdate-message"></a>WM_NCPOINTERUPDATE Meldung

Wird veröffentlicht, um ein Update für einen Zeiger bereitzustellen, der den Kontakt über den Nicht-Clientbereich eines Fensters hergestellt hat oder wenn ein nicht gekapselter Kontakt mit dem Mauszeiger über den Nicht-Clientbereich eines Fensters bewegt wird. Während der Zeiger zeigt, ist die Nachricht auf das Fenster ausgerichtet, in dem sich der Zeiger befindet. Während der Zeiger mit der Oberfläche in Kontakt steht, wird der Zeiger implizit auf das Fenster erfasst, über das der Zeiger Kontakt hergestellt hat, und dieses Fenster empfängt weiterhin Eingaben für den Zeiger, bis er den Kontakt unterbricht.

Wenn ein Fenster diesen Zeiger erfasst hat, wird diese Meldung nicht gesendet. Stattdessen wird ein [**WM_POINTERUPDATE**](wm-pointerupdate.md) an das Fenster gesendet, das diesen Zeiger erfasst hat.

> \[! Wichtig\]  
> Desktop-Apps sollten DPI-fähige Apps sein. Wenn Ihre App nicht DPI-bewusst ist, können Bildschirmkoordinaten, die in Zeigermeldungen und zugehörigen Strukturen enthalten sind, aufgrund der DPI-Virtualisierung ungenau erscheinen. Die DPI-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht DPI-bewusst sind und standardmäßig aktiv sind (Benutzer können sie deaktivieren). Weitere Informationen finden Sie unter [Schreiben von Win32-Anwendungen mit hohem DPI-Anteil.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define WM_NCPOINTERUPDATE                 0x0241
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Enthält den Zeigerbezeichner und zusätzliche Informationen. Verwenden Sie die folgenden Makros, um diese Informationen abzurufen.

[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Zeigerbezeichner

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): Treffertestwert, der von der Verarbeitung der [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) Meldung zurückgegeben wurde.

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

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte sie [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufrufen.

## <a name="remarks"></a>Hinweise

Wenn die Anwendung diese Nachricht nicht verarbeitet, führt [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) abhängig vom in der Nachricht enthaltenen Treffertestergebnis möglicherweise eine oder mehrere Systemaktionen aus. In der Regel sollten Anwendungen diese Meldung nicht verarbeiten müssen.

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

 

