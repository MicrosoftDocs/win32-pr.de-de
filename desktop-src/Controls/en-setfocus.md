---
title: EN_SETFOCUS Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn ein Bearbeitungs Steuerelement den Tastaturfokus erhält. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM- \_ Befehls Meldung.
ms.assetid: 482d2afa-4e21-4f3f-bdf4-6966b34cc3c4
keywords:
- Windows-Steuerelemente für EN_SETFOCUS Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cb96482f0e42669658dde3a39637e3c2311619
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743033"
---
# <a name="en_setfocus-notification-code"></a>EN \_ SetFocus-Benachrichtigungs Code

Wird gesendet, wenn ein Bearbeitungs Steuerelement den Tastaturfokus erhält. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
EN_SETFOCUS

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

Das übergeordnete Fenster empfängt immer eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung für dieses Ereignis, es ist jedoch keine Benachrichtigungs Maske erforderlich, die mit EM-Einstellungs- [**\_ Maske**](em-seteventmask.md)gesendet wurde.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

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

[EN \_ killfokus](en-killfocus.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

