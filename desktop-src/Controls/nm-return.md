---
title: NM_RETURN Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement den Eingabefokus besitzt und dass der Benutzer die EINGABETASTE gedrückt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 2c4839bc-6b23-469b-978f-cdf5f7bc0549
keywords:
- Windows-Steuerelemente für NM_RETURN Benachrichtigungs
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c6cebd089873df5471c9b25710efafaab4d246f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518455"
---
# <a name="nm_return-notification-code"></a>NM \_ Rückgabe Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Steuer Elements, dass das Steuerelement den Eingabefokus besitzt und dass der Benutzer die EINGABETASTE gedrückt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_RETURN 

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



 

 





