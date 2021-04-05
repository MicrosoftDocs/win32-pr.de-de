---
title: EN_VSCROLL Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf die vertikale Schiebe Leiste eines Bearbeitungs Steuer Elements klickt oder wenn der Benutzer den Mauszeiger über das Bearbeitungs Steuerelement bewegt.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- Windows-Steuerelemente für EN_VSCROLL Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1f99b9ea05d037b5c00562a24bda1e434ce08d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859279"
---
# <a name="en_vscroll-notification-code"></a>EN \_ VScroll-Benachrichtigungs Code

Wird gesendet, wenn der Benutzer auf die vertikale Schiebe Leiste eines Bearbeitungs Steuer Elements klickt oder wenn der Benutzer den Mauszeiger über das Bearbeitungs Steuerelement bewegt. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung. Das übergeordnete Fenster wird benachrichtigt, bevor der Bildschirm aktualisiert wird.


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungs Steuer Elements. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Bearbeitungs Steuerelement.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird für die folgenden Mausereignisse auf der vertikalen Schiebe Leiste gesendet: Klicken Sie auf die Pfeil Schaltfläche, oder klicken Sie auf die Pfeil Schaltfläche und den Ziehpunkt. Die Meldung wird jedoch nicht gesendet, wenn Sie auf die Schiebe Leiste mit der Maus selbst klicken. Die Meldung wird auch gesendet, wenn ein Tastaturereignis eine Änderung im Ansichts Bereich des Bearbeitungs Steuer Elements bewirkt, z. b. durch Drücken von Start, Ende, Bild-auf, Bild-ab, Pfeil nach oben oder nach-unten-Taste.

Das Mausrad ist eine Maus mit einem mittelrad, das einen Bildlauf durchführt. Weitere Informationen finden Sie unter "das Mausrad" in [etwa Maus Eingaben](/windows/desktop/inputdev/about-mouse-input).

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Um en \_ VScroll-Benachrichtigungs Codes zu erhalten, geben Sie [**ENM- \_ Scroll**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht [**EM \_**](em-seteventmask.md) -Nachricht gesendet wird. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[EN \_ HScroll](en-hscroll.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Verwenden von Bearbeitungs Steuerelementen](using-edit-controls.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

