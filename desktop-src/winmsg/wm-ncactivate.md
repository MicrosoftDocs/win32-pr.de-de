---
description: Wird an ein Fenster gesendet, wenn sein Nichtclientbereich geändert werden muss, um einen aktiven oder inaktiven Zustand anzugeben.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: WM_NCACTIVATE Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095f0cc7f555b4daf80a67a2394e29286f32a49dcba687780e8747f5d1b193fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056000"
---
# <a name="wm_ncactivate-message"></a>WM \_ NCACTIVATE-Nachricht

Wird an ein Fenster gesendet, wenn sein Nichtclientbereich geändert werden muss, um einen aktiven oder inaktiven Zustand anzugeben.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, wann eine Titelleiste oder ein Symbol geändert werden muss, um einen aktiven oder inaktiven Zustand anzugeben. Wenn eine aktive Titelleiste oder ein aktives Symbol gezeichnet werden soll, ist der *wParam-Parameter* **TRUE.** Wenn eine inaktive Titelleiste oder ein Symbol gezeichnet werden soll, ist *wParam* **FALSE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Wenn ein [visueller Stil](../controls/themes-overview.md) für dieses Fenster aktiv ist, wird dieser Parameter nicht verwendet.

Wenn ein visueller Stil für dieses Fenster nicht aktiv ist, ist dieser Parameter ein Handle für einen optionalen Updatebereich für den Nichtclientbereich des Fensters. Wenn dieser Parameter auf -1 festgelegt ist, zeichnet [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) den Nichtclientbereich nicht erneut, um die Zustandsänderung widerzuspiegeln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn der *wParam-Parameter* **FALSE** ist, sollte eine Anwendung **TRUE** zurückgeben, um anzugeben, dass das System mit der Standardverarbeitung fortfahren soll, oder sie sollte **FALSE** zurückgeben, um die Änderung zu verhindern. Wenn *wParam* **TRUE** ist, wird der Rückgabewert ignoriert.

## <a name="remarks"></a>Hinweise

Die Verarbeitung von Nachrichten im Zusammenhang mit dem Nichtclientbereich eines Standardfensters wird nicht empfohlen, da die Anwendung alle erforderlichen Teile des Nichtclientbereichs für das Fenster zeichnen kann. Wenn eine Anwendung diese Nachricht verarbeitet, muss sie **TRUE** zurückgeben, um das System anzuweisen, die Änderung des aktiven Fensters abzuschließen. Wenn das Fenster minimiert wird, wenn diese Nachricht empfangen wird, sollte die Anwendung die Nachricht an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben.

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) zeichnet die Titelleiste oder den Symboltitel in ihren aktiven Farben, wenn der *wParam-Parameter* **TRUE** ist, und in den inaktiven Farben, wenn *wParam* **FALSE** ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
