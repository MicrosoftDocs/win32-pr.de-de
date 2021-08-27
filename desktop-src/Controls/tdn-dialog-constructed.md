---
title: TDN_DIALOG_CONSTRUCTED Benachrichtigungscode (Commctrl.h)
description: Wird von einem Aufgabendialogfeld gesendet, nachdem das Dialogfeld erstellt wurde und bevor es angezeigt wird. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: e8556039-a74d-4e33-931d-a63ad5b2d4b0
keywords:
- TDN_DIALOG_CONSTRUCTED Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TDN_DIALOG_CONSTRUCTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f9d2e6497c1ed13e653edbd84a6fae05690367721201b0a0024bd524460195
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104470"
---
# <a name="tdn_dialog_constructed-notification-code"></a>TDN \_ DIALOG \_ CONSTRUCTED-Benachrichtigungscode

Wird von einem Aufgabendialogfeld gesendet, nachdem das Dialogfeld erstellt wurde und bevor es angezeigt wird. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann.


```C++
TDN_DIALOG_CONSTRUCTED
     
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



 

 





