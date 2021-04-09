---
title: NM_KEYDOWN Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Steuerelement gesendet, wenn das Steuerelement den Tastaturfokus besitzt und der Benutzer eine Taste drückt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- Windows-Steuerelemente für NM_KEYDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 222a47733a60590e7d56ca0adba038164c430fab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858643"
---
# <a name="nm_keydown-notification-code"></a>NM- \_ KeyDown-Benachrichtigungs Code

Wird von einem Steuerelement gesendet, wenn das Steuerelement den Tastaturfokus besitzt und der Benutzer eine Taste drückt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmkey**](/windows/win32/api/commctrl/ns-commctrl-nmkey) -Struktur, die zusätzliche Informationen über den Schlüssel enthält, der den Benachrichtigungs Code verursacht hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass das Steuerelement den Schlüssel verarbeitet, andernfalls

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





