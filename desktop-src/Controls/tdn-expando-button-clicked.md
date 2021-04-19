---
title: TDN_EXPANDO_BUTTON_CLICKED Benachrichtigungs Code (kommctrl. h)
description: Wird vom Aufgaben Dialogfeld gesendet, wenn der Benutzer auf die Expando-Schaltfläche des Dialog Felds klickt. Diese Benachrichtigung wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: 15e2a9d0-9986-4fb1-a15e-dd4839e45146
keywords:
- Windows-Steuerelemente für TDN_EXPANDO_BUTTON_CLICKED Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_EXPANDO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3c36379a8efc40c7873d817b832705b3c1e084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346765"
---
# <a name="tdn_expando_button_clicked-notification-code"></a>TDN- \_ expando- \_ Schaltfläche mit \_ Klick

Wird vom Aufgaben Dialogfeld gesendet, wenn der Benutzer auf die Expando-Schaltfläche des Dialog Felds klickt. Diese Benachrichtigung wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.


```C++
TDN_EXPANDO_BUTTON_CLICKED
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **boolescher** Wert, der **true** ist, wenn das Dialogfeld erweitert ist, andernfalls **false** .

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Das Beispiel im Abschnitt Syntax zeigt die Umwandlung in wParam vor dem Senden der Benachrichtigung. **LPARAM** wird nicht verwendet und muss NULL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





