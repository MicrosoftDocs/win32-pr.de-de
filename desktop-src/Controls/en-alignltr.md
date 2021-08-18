---
title: EN_ALIGNLTR Benachrichtigungscode (Richedit.h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuerelements, dass die Absatzrichtung von links nach rechts geändert wurde. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer WM \_ COMMAND-Nachricht gesendet.
ms.assetid: 754ac2b5-bcec-487b-a1ab-b653f673830a
keywords:
- EN_ALIGNLTR Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- EN_ALIGNLTR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 884f2750501dc1670d2f8e0497a196276571328809d295a687b3518a34b38ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019448"
---
# <a name="en_alignltr-notification-code"></a>EN \_ ALIGNLTR-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuerelements, dass die Absatzrichtung von links nach rechts geändert wurde. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer [**WM \_ COMMAND-Nachricht**](/windows/desktop/menurc/wm-command) gesendet.


```C++
EN_ALIGNLTR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LOWORD enthält**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den Bezeichner des Rich-Edit-Steuerelements. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Rich-Edit-Steuerelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Benachrichtigungscode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EN \_ ALIGNRTL**](en-alignrtl.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

