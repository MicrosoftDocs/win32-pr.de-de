---
title: HDN_ITEMDBLCLICK Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Headersteuerelements, dass der Benutzer auf das Steuerelement doppelklickt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet. Nur Headersteuerelemente, die auf den HDS BUTTONS-Stil festgelegt sind, \_ senden diesen Benachrichtigungscode.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- HDN_ITEMDBLCLICK Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7117ceb8d17447eed8003f7da3dab70a17252c750bfb3885cd3f235a70b7bb53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544612"
---
# <a name="hdn_itemdblclick-notification-code"></a>HDN \_ ITEMDBLCLICK-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Headersteuerelements, dass der Benutzer auf das Steuerelement doppelklickt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. Nur Headersteuerelemente, die auf den [**HDS \_ BUTTONS-Stil**](header-control-styles.md) festgelegt sind, senden diesen Benachrichtigungscode.


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) die Informationen zu diesem Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **HDN \_ ITEMDBLCLICKW** (Unicode) und **HDN \_ ITEMDBLCLICKA** (ANSI)<br/>         |



 

 





