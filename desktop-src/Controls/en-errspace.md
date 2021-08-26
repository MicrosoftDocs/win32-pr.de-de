---
title: EN_ERRSPACE Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn ein Bearbeitungssteuerelement nicht genügend Arbeitsspeicher zuweisen kann, um eine bestimmte Anforderung zu erfüllen. Das übergeordnete Fenster des Bearbeitungssteuerelements empfängt diesen Benachrichtigungscode über eine WM \_ COMMAND-Meldung.
ms.assetid: 23a6eb10-a9d7-4fd5-9176-407c35e6f492
keywords:
- EN_ERRSPACE Benachrichtigungscode Windows-Steuerelemente
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
ms.openlocfilehash: 548270e6382befa8a202a94c625f8cea214025d41661305f290250d66a771cbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047770"
---
# <a name="en_errspace-notification-code"></a>EN \_ ERRSPACE-Benachrichtigungscode

Wird gesendet, wenn ein Bearbeitungssteuerelement nicht genügend Arbeitsspeicher zuweisen kann, um eine bestimmte Anforderung zu erfüllen. Das übergeordnete Fenster des Bearbeitungssteuerelements empfängt diesen Benachrichtigungscode über eine [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
EN_ERRSPACE

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

Das übergeordnete Fenster erhält immer eine [**WM \_ COMMAND-Nachricht**](/windows/desktop/menurc/wm-command) für dieses Ereignis. Es ist keine Benachrichtigungsmaske erforderlich, die mit der [**EM \_ SETEVENTMASK-Nachricht**](em-seteventmask.md) gesendet wird.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

