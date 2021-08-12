---
title: STN_DISABLE Benachrichtigungscode (Winuser.h)
description: Der STN \_ DISABLE-Benachrichtigungscode wird gesendet, wenn ein statisches Steuerelement deaktiviert ist.
ms.assetid: 7ff0c191-4ff3-4a11-a418-8f45e16d0318
keywords:
- STN_DISABLE Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- STN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 793c4faaba723955d079891458b0d1823ca4fbd9c6053083cab5c886a1acbcb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670537"
---
# <a name="stn_disable-notification-code"></a>STN \_ DISABLE-Benachrichtigungscode

Der STN \_ DISABLE-Benachrichtigungscode wird gesendet, wenn ein statisches Steuerelement deaktiviert ist. Das statische Steuerelement muss über den [**SS \_ NOTIFY-Stil**](static-control-styles.md) verfügen, um diesen Benachrichtigungscode zu empfangen. Das übergeordnete Fenster des Steuerelements empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
STN_DISABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des statischen Steuerelements. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das statische Steuerelement.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[STN \_ ENABLE](stn-enable.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Statische Steuerelemente](static-controls.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

