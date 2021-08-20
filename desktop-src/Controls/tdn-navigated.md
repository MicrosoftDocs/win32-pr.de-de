---
title: TDN_NAVIGATED Benachrichtigungscode (Commctrl.h)
description: Wird von einem Aufgabendialogfeld gesendet, wenn die Navigation erfolgt ist. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: e7668ab3-3a11-4bf4-8cb4-067d3204fb3f
keywords:
- TDN_NAVIGATED Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TDN_NAVIGATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ee3daa29fa0f85db2dfb2a5991e0db9c9dba46938e69ad8d16153a97d400284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166893"
---
# <a name="tdn_navigated-notification-code"></a>TDN \_ NAVIGATED-Benachrichtigungscode

Wird von einem Aufgabendialogfeld gesendet, wenn die Navigation erfolgt ist. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann.


```C++
TDN_NAVIGATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





