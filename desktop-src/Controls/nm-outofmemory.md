---
title: NM_OUTOFMEMORY Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement einen Vorgang nicht beenden konnte, weil nicht genügend Arbeitsspeicher verfügbar war. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- Windows-Steuerelemente für NM_OUTOFMEMORY Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1321f88360d168b13d16b36f984d9b797dc094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040168"
---
# <a name="nm_outofmemory-notification-code"></a>NM- \_ oudefmemory-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement einen Vorgang nicht beenden konnte, weil nicht genügend Arbeitsspeicher verfügbar war. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird vom-Steuerelement ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





