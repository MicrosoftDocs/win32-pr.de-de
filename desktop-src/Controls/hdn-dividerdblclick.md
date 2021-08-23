---
title: HDN_DIVIDERDBLCLICK Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Headersteuerelements, dass der Benutzer auf den Unterteilerbereich des Steuerelements doppelklickt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- HDN_DIVIDERDBLCLICK Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b9ba7e974ce9e3adac2b48815bfb9bba5273db8298bc9948164be5904dca8a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544675"
---
# <a name="hdn_dividerdblclick-notification-code"></a>HDN \_ DIVIDERDBLCLICK-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Headersteuerelements, dass der Benutzer auf den Unterteilerbereich des Steuerelements doppelklickt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) die Informationen über das Headersteuerelement und das Element enthält, auf das doppelt geklickt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **HDN \_ DIVIDERDBLCLICKW** (Unicode) und **HDN \_ DIVIDERDBLCLICKA** (ANSI)<br/>   |



 

 





