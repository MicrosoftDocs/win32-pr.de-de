---
title: NM_CLICK (Statusleiste) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines StatusBar-Steuer Elements, dass der Benutzer auf die linke Maustaste im Steuerelement geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 179ccbe9-f51f-4356-b91a-10d7e3607b09
keywords:
- NM_CLICK (Statusleiste) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6066f76a8cf0b6ca34b5298cfcdcba2b11e3fa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859340"
---
# <a name="nm_click-status-bar-notification-code"></a>NM \_ Klick (Statusleiste) Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines StatusBar-Steuer Elements, dass der Benutzer auf die linke Maustaste im Steuerelement geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält. Der **dwitemspec** -Member enthält den Index des Abschnitts, auf den geklickt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um anzugeben, dass der Maus Klick behandelt wurde, und unterdrückt die Standard Verarbeitung durch das System. Gibt **false** zurück, um die Standard Verarbeitung des Click zuzulassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





