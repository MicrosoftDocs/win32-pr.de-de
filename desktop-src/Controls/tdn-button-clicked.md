---
title: TDN_BUTTON_CLICKED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer eine Schaltfläche oder einen Befehls Link im Aufgaben Dialogfeld auswählt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- Windows-Steuerelemente für TDN_BUTTON_CLICKED Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7a0b799f4163633194306edaa1703e068e93c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957182"
---
# <a name="tdn_button_clicked-notification-code"></a>TDN-Schaltfläche, auf die \_ \_ geklickt wird

Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer eine Schaltfläche oder einen Befehls Link im Aufgaben Dialogfeld auswählt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **int** -Wert, der die ID der ausgewählten Schaltfläche oder des Befehl-Links angibt.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Um zu verhindern, dass das Aufgaben Dialogfeld geschlossen wird, muss die Anwendung **S \_ false** zurückgeben. andernfalls wird das Aufgaben Dialogfeld geschlossen, und die Schaltflächen-ID wird über den ursprünglichen Anwendungs Befehl zurückgegeben

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





