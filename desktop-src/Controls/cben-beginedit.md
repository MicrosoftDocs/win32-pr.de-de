---
title: CBEN_BEGINEDIT Benachrichtigungscode (Commctrl.h)
description: Wird gesendet, wenn der Benutzer die Dropdownliste aktiviert oder auf das Bearbeitungsfeld des Steuerelements klickt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 77236471-b1c0-4679-b7b8-93e85867fe3b
keywords:
- CBEN_BEGINEDIT Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- CBEN_BEGINEDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109af3e9ccfdd7d8679ac7a5d467cafa966de6faf76adbd06450fd6ba782e80d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527900"
---
# <a name="cben_beginedit-notification-code"></a>CBEN \_ BEGINEDIT-Benachrichtigungscode

Wird gesendet, wenn der Benutzer die Dropdownliste aktiviert oder auf das Bearbeitungsfeld des Steuerelements klickt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
CBEN_BEGINEDIT

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die Informationen zum Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungscode verarbeitet, muss 0 (null) zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





