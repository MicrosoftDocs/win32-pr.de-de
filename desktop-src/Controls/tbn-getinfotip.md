---
title: TBN_GETINFOTIP Benachrichtigungscode (Commctrl.h)
description: Ruft Infotipinformationen für ein Symbolleistenelement ab. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6adb47a940ce6795047a1aca8bb7cbdc0899a142c132ab8f6f39e6bb089f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077904"
---
# <a name="tbn_getinfotip-notification-code"></a>TBN \_ GETINFOTIP-Benachrichtigungscode

Ruft Infotipinformationen für ein Symbolleistenelement ab. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTBGETINFOTIP-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) die Elementinformationen enthält und Infotip-Informationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird vom -Steuerelement ignoriert.

## <a name="remarks"></a>Hinweise

Die Infotip-Unterstützung auf der Symbolleiste ermöglicht es der Symbolleiste, QuickInfos für Elemente anzuzeigen, die so groß wie INFOTIPSIZE-Zeichen sind. Wenn dieser Benachrichtigungscode nicht verarbeitet wird, verwendet die Symbolleiste den Text des Elements für die Infotip.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TBN \_ GETINFOTIPW** (Unicode) und **TBN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





