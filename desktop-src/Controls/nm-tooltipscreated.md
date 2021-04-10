---
title: NM_TOOLTIPSCREATED Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement ein QuickInfo-Steuerelement erstellt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 8108f084-212d-4a16-b604-1ec134b1bb43
keywords:
- Windows-Steuerelemente für NM_TOOLTIPSCREATED Benachrichtigungs
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
ms.openlocfilehash: 6e2e99850b17b0f2b06948a09b70a89e67e65a50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040435"
---
# <a name="nm_tooltipscreated-notification-code"></a>NM- \_ tooltipscreated-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement ein QuickInfo-Steuerelement erstellt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmtooltipscreated**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Sofern nicht anders angegeben, ignoriert das Steuerelement den Rückgabewert aus diesem Benachrichtigungs Code.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





