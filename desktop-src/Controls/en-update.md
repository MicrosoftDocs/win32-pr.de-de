---
title: EN_UPDATE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn sich das Bearbeitungs Steuerelement selbst neu zeichnet.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- Windows-Steuerelemente für EN_UPDATE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105549"
---
# <a name="en_update-notification-code"></a>EN \_ Update-Benachrichtigungs Code

Wird gesendet, wenn sich das Bearbeitungs Steuerelement selbst neu zeichnet. Dieser Benachrichtigungs Code wird gesendet, nachdem das Steuerelement den Text formatiert hat, aber bevor der Text angezeigt wird. Dadurch ist es möglich, ggf. die Größe des Bearbeitungs Steuer Elements zu ändern. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
EN_UPDATE

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

**Rich Edit 1,0:** Zum Empfangen von en- \_ Update-Benachrichtigungs Codes geben Sie [**ENM- \_ Update**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der Nachricht [**EM \_**](em-seteventmask.md) -Nachricht gesendet wurde.

**Rich Edit 2,0 und höher:** Das Flag zum [**\_ Aktualisieren von SM**](rich-edit-control-event-mask-flags.md) wird ignoriert. Der en \_ Update-Benachrichtigungs Code wird immer empfangen. Wenn Microsoft Rich Edit 3,0 jedoch Microsoft Rich Edit 1,0 emuliert, müssen Sie zum Empfangen von en \_ Update-Benachrichtigungs Codes das **ENM- \_ Update** in der Maske angeben, die mit der Nachricht [**\_ EM**](em-seteventmask.md) -Nachricht gesendet wird.

Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

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

[\_Änderung der Änderung](en-change.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

