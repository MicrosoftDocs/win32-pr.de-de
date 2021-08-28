---
title: STN_DBLCLK Benachrichtigungscode (Winuser.h)
description: Der STN \_ DBLCLK-Benachrichtigungscode wird gesendet, wenn der Benutzer auf ein statisches Steuerelement mit dem \_ SS NOTIFY-Format doppelklickt. Das übergeordnete Fenster des Steuerelements empfängt diesen Benachrichtigungscode über die WM \_ COMMAND-Meldung.
ms.assetid: e3203309-87ea-46f4-9269-7e68c6fa0e4a
keywords:
- STN_DBLCLK Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- STN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a353d6ec47179cef43293e5babd2153ae5df27c9c844f7d5c91d78890e47713b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642570"
---
# <a name="stn_dblclk-notification-code"></a>STN \_ DBLCLK-Benachrichtigungscode

Der STN \_ DBLCLK-Benachrichtigungscode wird gesendet, wenn der Benutzer auf ein statisches Steuerelement mit dem [**SS \_ NOTIFY-Format**](static-control-styles.md) doppelklickt. Das übergeordnete Fenster des Steuerelements empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
STN_DBLCLK

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[STN \_ GEKLICKT](stn-clicked.md)
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

 

