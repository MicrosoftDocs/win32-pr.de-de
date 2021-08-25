---
title: TDN_HYPERLINK_CLICKED Benachrichtigungscode (Commctrl.h)
description: Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer im Inhalt des Aufgabendialogfelds auf einen Link klickt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: b769af31-32d0-463e-be15-6abf5dcb425c
keywords:
- TDN_HYPERLINK_CLICKED Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- TDN_HYPERLINK_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adaf5ecf05b22e3ff33aa88e28cb3f8f8c8b78f0b06d2127792b7639942bf7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875770"
---
# <a name="tdn_hyperlink_clicked-notification-code"></a>TDN \_ HYPERLINK \_ CLICKED notification code

Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer im Inhalt des Aufgabendialogfelds auf einen Link klickt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) registriert werden kann.


```C++
TDN_HYPERLINK_CLICKED

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

Zeiger auf eine Zeichenfolge mit Breitzeichen, die die URL des Links enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





