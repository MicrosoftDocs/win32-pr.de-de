---
title: NM_RELEASEDCAPTURE (Pager)-Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Pager-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigegeben hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 5ce9c38a-5d37-4ac7-8510-30bc59d85cca
keywords:
- NM_RELEASEDCAPTURE (Pager)-Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb1d258d9baa0952e1707e36884a492ff65f99b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858959"
---
# <a name="nm_releasedcapture-pager-notification-code"></a>NM \_ releasedcapture (Pager)-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Pager-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigegeben hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird vom Pager-Steuerelement ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





