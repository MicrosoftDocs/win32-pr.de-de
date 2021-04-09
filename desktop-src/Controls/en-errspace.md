---
title: EN_ERRSPACE Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn ein Bearbeitungs Steuerelement nicht genügend Arbeitsspeicher zuordnen kann, um eine bestimmte Anforderung zu erfüllen. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine WM- \_ Befehls Meldung.
ms.assetid: 23a6eb10-a9d7-4fd5-9176-407c35e6f492
keywords:
- Windows-Steuerelemente für EN_ERRSPACE Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05b100811741ee5c5f6bf53eb49ff05b118de3c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858687"
---
# <a name="en_errspace-notification-code"></a>EN \_ errspace-Benachrichtigungs Code

Wird gesendet, wenn ein Bearbeitungs Steuerelement nicht genügend Arbeitsspeicher zuordnen kann, um eine bestimmte Anforderung zu erfüllen. Das übergeordnete Fenster des Bearbeitungs Steuer Elements empfängt diesen Benachrichtigungs Code über eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
EN_ERRSPACE

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

Das übergeordnete Fenster erhält immer eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung für dieses Ereignis. es ist keine Benachrichtigungs Maske erforderlich, die mit der EM-Nachricht " [**\_ tventmask**](em-seteventmask.md) " gesendet wird.

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

 

