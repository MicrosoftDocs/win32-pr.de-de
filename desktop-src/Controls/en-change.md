---
title: EN_CHANGE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer eine Aktion durchgeführt hat, die möglicherweise Text in einem Bearbeitungs Steuerelement geändert hat.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- Windows-Steuerelemente für EN_CHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ef26d1ec4f8ec1dc93e54d46b88c4fe7cc872b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858786"
---
# <a name="en_change-notification-code"></a>EN \_ Änderungs Benachrichtigungs Code

Wird gesendet, wenn der Benutzer eine Aktion durchgeführt hat, die möglicherweise Text in einem Bearbeitungs Steuerelement geändert hat. Im Gegensatz zum [en \_ Update](en-update.md) -Benachrichtigungs Code wird dieser Benachrichtigungs Code gesendet, nachdem das System den Bildschirm aktualisiert hat. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
EN_CHANGE

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

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Um \_ Änderungs Benachrichtigungs Codes von en zu erhalten, geben Sie [**ENM- \_ Änderung**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_**](em-seteventmask.md) -Nachricht gesendet wurde. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

Der \_ Änderungs Benachrichtigungs Code von en wird nicht gesendet, wenn der [**\_ mehrzeilige**](edit-control-styles.md) Stil von es verwendet wird und der Text über [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext)gesendet wird.

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

[EN \_ Aktualisieren](en-update.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

