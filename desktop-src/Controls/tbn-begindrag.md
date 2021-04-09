---
title: TBN_BEGINDRAG Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer mit dem Ziehen einer Schaltfläche auf einer Symbolleiste begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 244406e5-e13d-4c80-81fa-81b018b29ec1
keywords:
- Windows-Steuerelemente für TBN_BEGINDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cfa7325d1a8e1eab27383d7df918c8896933bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103218"
---
# <a name="tbn_begindrag-notification-code"></a>TBN- \_ BeginDrag-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer mit dem Ziehen einer Schaltfläche auf einer Symbolleiste begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_BEGINDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur. Der **iItem** -Member enthält den Befehls Bezeichner der gezogenen Schaltfläche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





