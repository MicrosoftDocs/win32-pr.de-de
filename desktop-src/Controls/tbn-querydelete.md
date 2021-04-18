---
title: TBN_QUERYDELETE Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob eine Schaltfläche aus einer Symbolleiste gelöscht werden kann, während der Benutzer die Symbolleiste anpasst. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- Windows-Steuerelemente für TBN_QUERYDELETE Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517360"
---
# <a name="tbn_querydelete-notification-code"></a>TBN- \_ querydelete-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob eine Schaltfläche aus einer Symbolleiste gelöscht werden kann, während der Benutzer die Symbolleiste anpasst. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur. Das **iItem** -Member enthält den nullbasierten Index der zu löschenden Schaltfläche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um das Löschen der Schaltfläche zuzulassen, oder **false** , um zu verhindern, dass die Schaltfläche gelöscht wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





