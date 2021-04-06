---
title: EN_HSCROLL Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf die horizontale Schiebe Leiste eines Bearbeitungs Steuer Elements klickt. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM- \_ Befehls Meldung. Das übergeordnete Fenster wird benachrichtigt, bevor der Bildschirm aktualisiert wird.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- Windows-Steuerelemente für EN_HSCROLL Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f90f6e781409419e39390e64251506b4cc915a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859007"
---
# <a name="en_hscroll-notification-code"></a>EN \_ HScroll-Benachrichtigungs Code

Wird gesendet, wenn der Benutzer auf die horizontale Schiebe Leiste eines Bearbeitungs Steuer Elements klickt. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung. Das übergeordnete Fenster wird benachrichtigt, bevor der Bildschirm aktualisiert wird.


```C++
EN_HSCROLL

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

Dieser Benachrichtigungs Code wird für die folgenden Mausereignisse auf der horizontalen Schiebe Leiste gesendet: Klicken Sie auf die Pfeil Schaltfläche, oder klicken Sie auf die Pfeil Schaltfläche und den Ziehpunkt. Der Benachrichtigungs Code wird jedoch nicht gesendet, wenn Sie auf den Ziehpunkt der Bild Lauf Leiste selbst klicken. Der Benachrichtigungs Code wird auch gesendet, wenn ein Tastaturereignis eine Änderung im Ansichts Bereich des Bearbeitungs Steuer Elements bewirkt, z. b. durch Drücken von Start, Ende, Pfeil nach links oder nach rechts.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Geben Sie zum Empfangen von **en \_ HScroll** -Benachrichtigungs Codes [**ENM- \_ Scroll**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht [**EM \_**](em-seteventmask.md) -Abmeldung gesendet wird. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

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

[EN \_ VScroll](en-vscroll.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

