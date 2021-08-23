---
title: EN_UPDATE Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn sich ein Bearbeitungssteuerelement gerade neu zeichnet.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- EN_UPDATE Benachrichtigungscode Windows-Steuerelemente
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
ms.openlocfilehash: c126122336fd878dda633620c395cb86c112de1f5dc89e8e25d2c4e08bd93ebd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436429"
---
# <a name="en_update-notification-code"></a>EN \_ UPDATE-Benachrichtigungscode

Wird gesendet, wenn sich ein Bearbeitungssteuerelement gerade neu zeichnet. Dieser Benachrichtigungscode wird gesendet, nachdem das Steuerelement den Text formatiert hat, aber bevor der Text angezeigt wird. Dadurch kann bei Bedarf die Größe des Bearbeitungssteuerelementfensters geändert werden. Das übergeordnete Fenster des Bearbeitungssteuerelements empfängt diesen Benachrichtigungscode über eine [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
EN_UPDATE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Bearbeitungssteuerelements. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Bearbeitungssteuerelement.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**Rich Edit 1.0:** Um EN \_ UPDATE-Benachrichtigungscodes zu empfangen, geben Sie [**ENM \_ UPDATE**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht**](em-seteventmask.md) gesendet wird.

**Rich Edit 2.0 und höher:** Das [**ENM \_ UPDATE-Flag**](rich-edit-control-event-mask-flags.md) wird ignoriert. Der \_ EN UPDATE-Benachrichtigungscode wird immer empfangen. Wenn Microsoft Rich Edit 3.0 jedoch Microsoft Rich Edit 1.0 emuliert, müssen Sie zum Empfangen von EN \_ UPDATE-Benachrichtigungscodes **ENM \_ UPDATE** in der Maske angeben, die mit der [**EM \_ SETEVENTMASK-Nachricht**](em-seteventmask.md) gesendet wird.

Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Referenz**
</dt> <dt>

[EN \_ CHANGE](en-change.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

