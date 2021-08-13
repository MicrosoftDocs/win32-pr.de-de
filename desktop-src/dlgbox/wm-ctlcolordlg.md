---
title: WM_CTLCOLORDLG Meldung (Winuser.h)
description: Wird an ein Dialogfeld gesendet, bevor das System das Dialogfeld zeichnet. Durch Reagieren auf diese Meldung kann das Dialogfeld mithilfe des angegebenen Anzeigegerätekontexthandle seine Text- und Hintergrundfarben festlegen.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- Dialogfelder für WM_CTLCOLORDLG Meldung
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b7ab11bbb2cfd402888f930d5bcf2afa08b7ba83f74252fb3e443fd9e9309a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503413"
---
# <a name="wm_ctlcolordlg-message"></a>WM \_ CTLCOLORDLG-Nachricht

Wird an ein Dialogfeld gesendet, bevor das System das Dialogfeld zeichnet. Durch Reagieren auf diese Meldung kann das Dialogfeld mithilfe des angegebenen Anzeigegerätekontexthandle seine Text- und Hintergrundfarben festlegen.


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für den Gerätekontext für das Dialogfeld.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle des Dialogfelds.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, muss sie ein Handle an einen Pinsel zurückgeben. Das System verwendet den Pinsel, um den Hintergrund des Dialogfelds zu zeichnen.

## <a name="remarks"></a>Hinweise

Standardmäßig wählt die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die Standardsystemfarben für das Dialogfeld aus.

Das System zerstört den zurückgegebenen Pinsel nicht automatisch. Es liegt in der Verantwortung der Anwendung, den Pinsel zu zerstören, wenn er nicht mehr benötigt wird.

Die **WM \_ CTLCOLORDLG-Nachricht** wird nie zwischen Threads gesendet. Er wird nur innerhalb eines Threads gesendet.

Beachten Sie, dass die **WM \_ CTLCOLORDLG-Nachricht** an das Dialogfeld selbst gesendet wird. Alle anderen **WM \_ \* CTLCOLOR-Nachrichten** werden an den Besitzer des Steuerelements gesendet.

Wenn eine Dialogfeldprozedur diese Meldung verarbeitet, sollte sie den gewünschten Rückgabewert in einen **INT \_ PTR-Wert** konvertieren und den Wert direkt zurückgeben. Wenn die Dialogfeldprozedur **FALSE** zurückgibt, wird die Standardmäßige Nachrichtenverarbeitung ausgeführt. Der von der [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) festgelegte **\_ DWL-MSGRESULT-Wert** wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Dialogfelder](dialog-boxes.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**Wählen SiePalette aus.**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

