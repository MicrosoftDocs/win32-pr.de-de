---
title: EN_ALIGNRTL Benachrichtigungscode (Richedit.h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuerelements, dass die Absatzrichtung von rechts nach links geändert wurde. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer WM \_ COMMAND-Nachricht gesendet.
ms.assetid: 2db5fd49-9ecd-49d7-8199-1706648255ca
keywords:
- EN_ALIGNRTL Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- EN_ALIGNRTL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179b9a610d2d834081ddd246ea4d649c099a8df3a62d21815c825bd55701dad2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799850"
---
# <a name="en_alignrtl-notification-code"></a>EN \_ ALIGNRTL-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuerelements, dass die Absatzrichtung von rechts nach links geändert wurde. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer [**WM \_ COMMAND-Nachricht**](/windows/desktop/menurc/wm-command) gesendet.


```C++
EN_ALIGNRTL

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EN \_ ALIGNLTR**](en-alignltr.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

