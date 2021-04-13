---
title: NM_RCLICK (Statusleiste) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Status leisten-Steuer Elements, dass der Benutzer mit der rechten Maustaste im-Steuerelement geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 9a441d32-f4e4-42ae-877f-17079b0188f4
keywords:
- NM_RCLICK (Statusleiste) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326ac6600716419648ecfacf25cd8423551fd03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341368"
---
# <a name="nm_rclick-status-bar-notification-code"></a>NM \_ rclick-Benachrichtigungs Code (Statusleiste)

Benachrichtigt das übergeordnete Fenster eines Status leisten-Steuer Elements, dass der Benutzer mit der rechten Maustaste im-Steuerelement geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_RCLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um anzugeben, dass der Maus Klick behandelt wurde, und unterdrückt die Standard Verarbeitung durch das System. Gibt **false** zurück, um die Standard Verarbeitung des Click zuzulassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





