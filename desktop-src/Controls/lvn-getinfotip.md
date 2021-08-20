---
title: LVN_GETINFOTIP Benachrichtigungscode (Commctrl.h)
description: Wird von einem großen Symbolansichts-Listenansicht-Steuerelement gesendet, das den \_ \_ erweiterten LVS EX INFOTIP-Stil auflistet.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f7477230913ec5efd0827bc48e1a6021619aa4cdbbad252426d1af364b5b36b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830441"
---
# <a name="lvn_getinfotip-notification-code"></a>LVN \_ GETINFOTIP-Benachrichtigungscode

Wird von einem großen Symbolansichts-Listenansicht-Steuerelement gesendet, das den [**erweiterten LVS \_ EX \_ INFOTIP-Stil**](extended-list-view-styles.md) auflistet. Dieser Benachrichtigungscode wird gesendet, wenn das Listenansicht-Steuerelement zusätzliche Textinformationen anfordert, die in einer QuickInfo angezeigt werden sollen. Sie wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLVGETINFOTIP-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) die Informationen zu diesem Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Dieser Benachrichtigungscode wird nur von Listenansichtssteuerelementen gesendet, die den [**erweiterten LVS \_ EX \_ INFOTIP-Stil**](extended-list-view-styles.md) aufweisen. Der \_ LVN-GETINFOTIP-Benachrichtigungscode wird nur für Unteritem 0 gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVN \_ GETINFOTIPW** (Unicode) und **LVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





