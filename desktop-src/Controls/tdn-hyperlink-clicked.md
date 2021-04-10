---
title: TDN_HYPERLINK_CLICKED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer auf einen Link im Inhalt des Aufgaben Dialogfelds klickt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: b769af31-32d0-463e-be15-6abf5dcb425c
keywords:
- Windows-Steuerelemente für TDN_HYPERLINK_CLICKED Benachrichtigungs
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
ms.openlocfilehash: edd79406eb59f9bafd93269f8982db6213ef882c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106233"
---
# <a name="tdn_hyperlink_clicked-notification-code"></a>Von TDN \_ \_ angeklickte Benachrichtigungs Code

Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer auf einen Link im Inhalt des Aufgaben Dialogfelds klickt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.


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

Zeiger auf eine breit Zeichen-Zeichenfolge, die die URL des Links enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





