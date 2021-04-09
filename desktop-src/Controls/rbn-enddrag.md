---
title: RBN_ENDDRAG Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, wenn der Benutzer das Ziehen eines Bands beendet. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 24b06144-6a4c-46a4-bef1-d6592f72a2c0
keywords:
- Windows-Steuerelemente für RBN_ENDDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb6c538679d793ed2407775b4238cea475ba4ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040791"
---
# <a name="rbn_enddrag-notification-code"></a>RBN- \_ EndDrag-Benachrichtigungs Code

Wird von einem Grund leisten-Steuerelement gesendet, wenn der Benutzer das Ziehen eines Bands beendet. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
RBN_ENDDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmrebar**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) -Struktur, die Informationen über den Benachrichtigungs Code enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diesen Benachrichtigungs Code wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





