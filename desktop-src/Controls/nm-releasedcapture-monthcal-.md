---
title: NM_RELEASEDCAPTURE (monthcal)-Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines monthcal-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: c05d3331-26f3-41f4-8032-36ed38d47917
keywords:
- NM_RELEASEDCAPTURE (monthcal)-Benachrichtigungs Code Windows-Steuerelemente
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
ms.openlocfilehash: 0b9c743a076c8046aa57ba4306145248ed00f0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739920"
---
# <a name="nm_releasedcapture-monthcal-notification-code"></a>NM \_ releasedcapture (monthcal)-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines monthcal-Steuer Elements, dass das Steuerelement die Maus Aufzeichnung freigibt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


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

Das-Steuerelement ignoriert den Rückgabewert aus diesem Benachrichtigungs Code.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





