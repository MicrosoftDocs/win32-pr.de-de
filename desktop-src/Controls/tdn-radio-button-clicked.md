---
title: TDN_RADIO_BUTTON_CLICKED Benachrichtigungscode (Commctrl.h)
description: Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer ein Optionsfeld oder einen Befehlslink im Aufgabendialogfeld auswählt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: d9a29874-6755-4754-bcaf-94746b218b47
keywords:
- TDN_RADIO_BUTTON_CLICKED Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TDN_RADIO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea1917a1523cdc3a106398d07912d3fff5295f7da18a59055f059a13007f98b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875760"
---
# <a name="tdn_radio_button_clicked-notification-code"></a>TDN \_ \_ OPTIONSFELD \_ KLICKT Benachrichtigungscode

Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer ein Optionsfeld oder einen Befehlslink im Aufgabendialogfeld auswählt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) registriert werden kann.


```C++
TDN_RADIO_BUTTON_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Wert vom Wert **int,** der die ID angibt, die dem Optionsfeld entspricht, auf das geklickt wurde.

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



 

 





