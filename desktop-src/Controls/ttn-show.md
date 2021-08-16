---
title: TTN_SHOW Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das Besitzerfenster, dass ein QuickInfo-Steuerelement angezeigt wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74397223f20668487e78cea15e2e1507026ee65089e5011065b3f177514e899b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408812"
---
# <a name="ttn_show-notification-code"></a>TTN \_ SHOW-Benachrichtigungscode

Benachrichtigt das Besitzerfenster, dass ein QuickInfo-Steuerelement angezeigt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR-Struktur.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

[Version 4.70.](common-control-versions.md) Um die QuickInfo am Standardspeicherort anzuzeigen, geben Sie 0 (null) zurück. Um die QuickInfo-Position anzupassen, positionieren Sie das QuickInfo-Fenster mit der [**SetWindowPos-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) neu, und geben **Sie TRUE** zurück.

> [!Note]  
> Für Versionen vor 4.70 gibt es keinen Rückgabewert.

 

## <a name="remarks"></a>Hinweise

Ein QuickInfo-Fensterrechteck ist etwas größer als sein Textanzeigerechteck, und sein Ursprung wird nach oben und links versetzt. Wenn Sie das Textanzeigerechteck einer QuickInfo genau positionieren müssen, konvertiert die [**TTM \_ ADJUSTRECT-Nachricht**](ttm-adjustrect.md) ein Textanzeigerechteck in das entsprechende QuickInfo-Fensterrechteck und umgekehrt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

