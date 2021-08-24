---
title: NM_TOOLTIPSCREATED -Benachrichtigungscode (Symbolleiste) (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die Symbolleiste ein QuickInfo-Steuerelement erstellt hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- NM_TOOLTIPSCREATED -Benachrichtigungscode (Symbolleiste) Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa40313a8b8c11c48b37cf2ae0593cb1bbc85353303f7c8840e7e5eb55ea7ca9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877280"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a>NM \_ TOOLTIPSCREATED (Symbolleiste) – Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die Symbolleiste ein QuickInfo-Steuerelement erstellt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTOOLTIPSCREATED-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Das Symbolleistensteuerelement ignoriert den Rückgabewert dieses Benachrichtigungscodes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





