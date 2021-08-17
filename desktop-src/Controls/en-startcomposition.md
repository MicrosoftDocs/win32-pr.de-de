---
title: EN_STARTCOMPOSITION Benachrichtigungscode (Richedit.h)
description: Benachrichtigt ein übergeordnetes Fenster des Rich-Edit-Steuerelements, dass der Benutzer mit der Eingabe von IME oder Textdienstframework.
ms.assetid: 755C0C5F-061B-44AF-98A5-776AEE1B7AF8
keywords:
- EN_STARTCOMPOSITION Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- EN_STARTCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b182322175d03ab1c6906132c8f5970ce1d716e7e1c745406b009e5b224ec2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436670"
---
# <a name="en_startcomposition-notification-code"></a>EN \_ STARTCOMPOSITION-Benachrichtigungscode

Benachrichtigt ein übergeordnetes Fenster mit rich edit-Steuerelementen, dass der Benutzer mit der Eingabe von ime oder [Textdienstframework.](/windows/desktop/TSF/text-services-framework)


```C++
EN_STARTCOMPOSITION

    pStartComp = (NMDHR *) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**NMHDR-Struktur.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

