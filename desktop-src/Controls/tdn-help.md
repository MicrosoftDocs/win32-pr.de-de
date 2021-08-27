---
title: TDN_HELP Benachrichtigungscode (Commctrl.h)
description: Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer F1 auf der Tastatur drückt, während der Dialog den Fokus besitzt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: 207ba231-639d-4906-b5dc-1592f2717f1c
keywords:
- TDN_HELP Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TDN_HELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5944fb136a76b880deb51b461a0e48b8d81ce2aca541cb6fa3717c3d79e9ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104460"
---
# <a name="tdn_help-notification-code"></a>TDN \_ HELP-Benachrichtigungscode

Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer F1 auf der Tastatur drückt, während der Dialog den Fokus besitzt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) registriert werden kann.


```C++
TDN_HELP
        
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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





