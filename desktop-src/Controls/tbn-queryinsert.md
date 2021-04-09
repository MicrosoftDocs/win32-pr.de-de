---
title: TBN_QUERYINSERT Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob links neben der angegebenen Schaltfläche eine Schaltfläche eingefügt werden kann, während der Benutzer eine Symbolleiste anpasst. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- Windows-Steuerelemente für TBN_QUERYINSERT Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957101"
---
# <a name="tbn_queryinsert-notification-code"></a>TBN \_ queryinsert-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster der Symbolleiste, ob links neben der angegebenen Schaltfläche eine Schaltfläche eingefügt werden kann, während der Benutzer eine Symbolleiste anpasst. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur. Das **iItem** -Member enthält den nullbasierten Index der einzufügenden Schaltfläche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um zuzulassen, dass eine Schaltfläche vor der angegebenen Schaltfläche eingefügt wird, oder **false** , um zu verhindern, dass die Schaltfläche eingefügt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





