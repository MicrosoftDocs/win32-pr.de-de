---
title: HDN_ENDDRAG Benachrichtigungscode (Commctrl.h)
description: Wird von einem Headersteuerelementen gesendet, wenn ein Ziehvorgang für eines seiner Elemente beendet wurde. Dieser Benachrichtigungscode wird als WM \_ NOTIFY-Nachricht gesendet. Nur Headersteuerelemente, die auf den HDS \_ DRAGDROP-Stil festgelegt sind, senden diesen Benachrichtigungscode.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- HDN_ENDDRAG Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df56beb0b5b4a75716723330711714b7db9f4f27100ffe3296626d2be5798a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544618"
---
# <a name="hdn_enddrag-notification-code"></a>HDN \_ ENDDRAG-Benachrichtigungscode

Wird von einem Headersteuerelementen gesendet, wenn ein Ziehvorgang für eines seiner Elemente beendet wurde. Dieser Benachrichtigungscode wird als [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. Nur Headersteuerelemente, die auf den [**HDS \_ DRAGDROP-Stil**](header-control-styles.md) festgelegt sind, senden diesen Benachrichtigungscode.


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) die Informationen über das header-Element enthält, das gezogen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Damit das Steuerelement das Element automatisch platzieren und neu anordnen kann, geben Sie **FALSE zurück.** Um zu verhindern, dass das Element platziert wird, geben Sie **TRUE zurück.**

## <a name="remarks"></a>Hinweise

If the owner is performing external (manual) drag-and-drop management, it must return **FALSE**. Der Besitzer muss Headerelemente dann manuell neu anordnen, indem er [**HDM \_ SETITEM**](hdm-setitem.md) oder [**HDM \_ SETORDERARRAY sendet.**](hdm-setorderarray.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





