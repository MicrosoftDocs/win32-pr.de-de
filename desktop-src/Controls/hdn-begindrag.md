---
title: HDN_BEGINDRAG Benachrichtigungscode (Commctrl.h)
description: Wird von einem Headersteuerelementen gesendet, wenn ein Ziehvorgang für eines seiner Elemente begonnen hat. Dieser Benachrichtigungscode wird nur von Headersteuerelementen gesendet, die auf den HDS \_ DRAGDROP-Stil festgelegt sind. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- HDN_BEGINDRAG Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae1ab3f8ac24b5521fab1afc5313503867e575906e851acf4d4fdbe90fe787d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544690"
---
# <a name="hdn_begindrag-notification-code"></a>HDN \_ BEGINDRAG-Benachrichtigungscode

Wird von einem Headersteuerelementen gesendet, wenn ein Ziehvorgang für eines seiner Elemente begonnen hat. Dieser Benachrichtigungscode wird nur von Headersteuerelementen gesendet, die auf den [**HDS \_ DRAGDROP-Stil festgelegt**](header-control-styles.md) sind. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) die Informationen über das header-Element enthält, das gezogen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

To allow the header control to automatically manage drag-and-drop operations, return **FALSE**. If the owner of the control is manually performing drag-and-drop reordering, return **TRUE**.

## <a name="remarks"></a>Hinweise

Ein Header-Steuerelement führt standardmäßig die automatische Verwaltung der Drag & Drop-Neuanordnung durch. Returning **TRUE** to indicate external (manual) drag-and-drop management allows the owner of the control to provide custom services as part of the drag-and-drop process.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





