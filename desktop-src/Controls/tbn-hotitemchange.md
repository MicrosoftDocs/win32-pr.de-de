---
title: TBN_HOTITEMCHANGE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem ToolBar-Steuerelement gesendet, wenn sich das heiße Element (hervorgehoben) ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- Windows-Steuerelemente für TBN_HOTITEMCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314a7250128a0f3e6b3fed54e5765487619d8e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739889"
---
# <a name="tbn_hotitemchange-notification-code"></a>TBN- \_ meldeänderungs-Benachrichtigungs Code

Wird von einem ToolBar-Steuerelement gesendet, wenn sich das heiße Element (hervorgehoben) ändert. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtbhutitem**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt NULL zurück, damit das Element hervorgehoben werden kann, oder ungleich NULL, um zu verhindern, dass das Element hervorgehoben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





