---
title: RBN_MINMAX Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, bevor ein Band maximiert oder minimiert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- Windows-Steuerelemente für RBN_MINMAX Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3569a28d0c0a610ccccf42d11ff4b2e5b4b0007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341391"
---
# <a name="rbn_minmax-notification-code"></a>RBN- \_ MinMax-Benachrichtigungs Code

Wird von einem Grund leisten-Steuerelement gesendet, bevor ein Band maximiert oder minimiert wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
RBN_MINMAX
```



## <a name="parameters"></a>Parameter

Dieser Benachrichtigungs Code weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass der Vorgang stattfindet, und NULL, um den Vorgang fortzusetzen

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





