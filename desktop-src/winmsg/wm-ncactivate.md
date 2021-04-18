---
description: Wird an ein Fenster gesendet, wenn der nicht-Client Bereich geändert werden muss, um einen aktiven oder inaktiven Zustand anzugeben.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: WM_NCACTIVATE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368755"
---
# <a name="wm_ncactivate-message"></a>WM- \_ ncaktivierungs Meldung

Wird an ein Fenster gesendet, wenn der nicht-Client Bereich geändert werden muss, um einen aktiven oder inaktiven Zustand anzugeben.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, wann eine Titelleiste oder ein Symbol geändert werden muss, um einen aktiven oder inaktiven Zustand anzugeben. Wenn eine aktive Titelleiste oder ein Symbol gezeichnet werden soll, ist der *wParam* -Parameter **true**. Wenn eine inaktive Titelleiste oder ein Symbol gezeichnet werden soll, ist *wParam* auf **false** gesetzt.

</dd> <dt>

*lParam* 
</dt> <dd>

Wenn ein [visueller Stil](../controls/themes-overview.md) für dieses Fenster aktiv ist, wird dieser Parameter nicht verwendet.

Wenn ein visueller Stil für dieses Fenster nicht aktiv ist, ist dieser Parameter ein Handle für einen optionalen Update Bereich für den nicht-Client Bereich des Fensters. Wenn dieser Parameter auf-1 festgelegt ist, zeichnet [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) den nicht-Client Bereich nicht neu, um die Statusänderung widerzuspiegeln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn der *wParam* -Parameter den Wert **false** hat, sollte eine Anwendung **true** zurückgeben, um anzugeben, dass das System die Standard Verarbeitung fortsetzen soll, oder es sollte **false** zurückgeben, um die Änderung zu verhindern. Wenn *wParam* den Wert **true** hat, wird der Rückgabewert ignoriert.

## <a name="remarks"></a>Bemerkungen

Das Verarbeiten von Nachrichten, die sich auf den nicht-Client Bereich eines Standard Fensters beziehen, wird nicht empfohlen, da die Anwendung alle erforderlichen Teile des nicht-Client Bereichs für das Fenster zeichnen muss. Wenn eine Anwendung diese Nachricht verarbeitet, muss Sie " **true** " zurückgeben, um das System zum Abschluss der Änderung des aktiven Fensters zu leiten. Wenn das Fenster beim Empfang dieser Nachricht minimiert wird, sollte die Anwendung die Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben.

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion zeichnet die Titelleiste oder den Symbol Titel in den aktiven Farben, wenn der *wParam* -Parameter **true** ist, und in den inaktiven Farben, wenn *wParam* den Wert **false** hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
