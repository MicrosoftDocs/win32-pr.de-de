---
title: STN_CLICKED Benachrichtigungscode (Winuser.h)
description: Der STN CLICKED-Benachrichtigungscode wird gesendet, wenn der Benutzer auf ein statisches Steuerelement klickt, das über den \_ Stil SS \_ NOTIFY verfügt. Das übergeordnete Fenster des Steuerelements empfängt diesen Benachrichtigungscode über die WM \_ COMMAND-Meldung.
ms.assetid: deeac9e9-c23e-4ffb-a1d7-18782efb7a5c
keywords:
- STN_CLICKED Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- STN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984bbe63444593707de7e410ebd9cb47fb60bac4766ea6ee57660f034e45924d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797870"
---
# <a name="stn_clicked-notification-code"></a>\_STN-Klickbenachrichtigungscode

Der STN CLICKED-Benachrichtigungscode wird gesendet, wenn der Benutzer auf ein statisches Steuerelement klickt, das über den \_ [**Stil SS \_ NOTIFY**](static-control-styles.md) verfügt. Das übergeordnete Fenster des Steuerelements empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
STN_CLICKED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LOWORD enthält**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den Bezeichner des statischen Steuerelements. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das statische Steuerelement.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[STN \_ DBLCLK](stn-dblclk.md)
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

 

