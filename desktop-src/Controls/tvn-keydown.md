---
title: TVN_KEYDOWN Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass der Benutzer eine Taste gedrückt hat und das Strukturansicht-Steuerelement den Eingabefokus besitzt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: da0d2b62-2295-4dce-9b37-a250f3be087f
keywords:
- TVN_KEYDOWN Benachrichtigungscode Windows Steuerelementen
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
ms.openlocfilehash: dadd3386e83e541288249b83028119111a42855a111f7ecb398571a1d46ab356
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002470"
---
# <a name="tvn_keydown-notification-code"></a>TVN \_ KEYDOWN-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass der Benutzer eine Taste gedrückt hat und das Strukturansicht-Steuerelement den Eingabefokus besitzt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_KEYDOWN 

    ptvkd = (LPNMTVKEYDOWN) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVKEYDOWN-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtvkeydown) Der **wVKey-Member** gibt den Code des virtuellen Schlüssels an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn das **wVKey-Member** von *lParam* ein Zeichenschlüsselcode ist, wird das Zeichen als Teil einer inkrementellen Suche verwendet. Geben Sie einen Wert ungleich 0 (null) zurück, um das Zeichen von der inkrementellen Suche auszuschließen, oder 0 (null), um das Zeichen in die Suche einschließt. Für alle anderen Schlüssel wird der Rückgabewert ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





