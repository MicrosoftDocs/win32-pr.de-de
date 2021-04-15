---
title: NM_TOOLTIPSCREATED (Symbolleisten-) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die Symbolleiste ein QuickInfo-Steuerelement erstellt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- NM_TOOLTIPSCREATED (Symbolleiste) Benachrichtigungs Code Windows-Steuerelemente
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
ms.openlocfilehash: c13366348da075fab48e7a2f12381f51f7d87bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476062"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a>NM- \_ tooltipscreated-Benachrichtigungs Code (Symbolleiste)

Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die Symbolleiste ein QuickInfo-Steuerelement erstellt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtooltipscreated**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Das Symbolleisten-Steuerelement ignoriert den Rückgabewert aus diesem Benachrichtigungs Code.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





