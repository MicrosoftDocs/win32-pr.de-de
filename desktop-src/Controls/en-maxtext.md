---
title: EN_MAXTEXT Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn die aktuelle Text Einfügung die angegebene Anzahl von Zeichen für das Bearbeitungs Steuerelement überschritten hat.
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- Windows-Steuerelemente für EN_MAXTEXT Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_MAXTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 454b48fb232f2225696efacc44d54660d3a83185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518659"
---
# <a name="en_maxtext-notification-code"></a>EN \_ maxtext-Benachrichtigungs Code

Wird gesendet, wenn die aktuelle Text Einfügung die angegebene Anzahl von Zeichen für das Bearbeitungs Steuerelement überschritten hat. Die Text Einfügung wurde abgeschnitten.

Dieser Benachrichtigungs Code wird auch gesendet, wenn ein Bearbeitungs Steuerelement nicht den " [**es \_ autohscroll**](edit-control-styles.md) "-Stil hat und die Anzahl der einzufügenden Zeichen die Breite des Bearbeitungs Steuer Elements überschreiten würde.

Dieser Benachrichtigungs Code wird auch gesendet, wenn ein Bearbeitungs Steuerelement nicht den " [**es \_ autovscroll**](edit-control-styles.md) "-Stil hat und die Gesamtanzahl der Zeilen, die sich aus einer Text Einfügung ergeben, die Höhe des Bearbeitungs Steuer Elements überschreiten würde.

Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
EN_MAXTEXT

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

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

