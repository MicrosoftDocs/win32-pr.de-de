---
title: EN_CHANGE Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn der Benutzer eine Aktion ergriffen hat, die möglicherweise Text in einem Bearbeitungssteuerfeld geändert hat.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- EN_CHANGE Benachrichtigungscode Windows Steuerelementen
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
ms.openlocfilehash: b86dbfb90376a85df09cad854882fa2616e6b7cb247cab4106850608a4b96ad4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437050"
---
# <a name="en_change-notification-code"></a>EN \_ CHANGE-Benachrichtigungscode

Wird gesendet, wenn der Benutzer eine Aktion ergriffen hat, die möglicherweise Text in einem Bearbeitungssteuerfeld geändert hat. Im Gegensatz [zum EN \_ UPDATE-Benachrichtigungscode](en-update.md) wird dieser Benachrichtigungscode gesendet, nachdem das System den Bildschirm aktualisiert hat. Das übergeordnete Fenster des Bearbeitungssteuer elements empfängt diesen Benachrichtigungscode über eine [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
EN_CHANGE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LOWORD enthält**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den Bezeichner des Bearbeitungssteuerzeichens. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für das Bearbeitungssteuer steuerelement.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Um EN \_ CHANGE-Benachrichtigungscodes zu erhalten, geben Sie [**ENM \_ CHANGE**](rich-edit-control-event-mask-flags.md) in der Maske an, die mit der [**EM \_ SETEVENTMASK-Nachricht gesendet**](em-seteventmask.md) wird. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

Der EN CHANGE-Benachrichtigungscode wird nicht gesendet, wenn das \_ [**ES \_ MULTILINE-Format**](edit-control-styles.md) verwendet wird und der Text über [**WM \_ SETTEXT gesendet wird.**](/windows/desktop/winmsg/wm-settext)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Referenz**
</dt> <dt>

[EN \_ UPDATE](en-update.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

