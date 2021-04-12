---
title: TVN_KEYDOWN Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass der Benutzer eine Taste gedrückt hat und das Strukturansicht-Steuerelement den Eingabefokus besitzt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- Windows-Steuerelemente für TVN_KEYDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ccb18c3bf7dc03056abb55575850821e11eb9bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475123"
---
# <a name="tvn_keydown-notification-code"></a>TVN- \_ KeyDown-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuer Elements, dass der Benutzer eine Taste gedrückt hat und das Strukturansicht-Steuerelement den Eingabefokus besitzt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtvkeydown**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) -Struktur. Der **wvkey** -Member gibt den Code des virtuellen Schlüssels an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der **wvkey** -Member von *LPARAM* ein Zeichen Schlüsselcode ist, wird das Zeichen im Rahmen einer inkrementellen Suche verwendet. Gibt einen Wert ungleich 0 (null) zurück, wenn das Zeichen aus der inkrementellen Suche ausgeschlossen werden soll Bei allen anderen Schlüsseln wird der Rückgabewert ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





