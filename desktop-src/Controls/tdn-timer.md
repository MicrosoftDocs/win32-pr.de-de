---
title: TDN_TIMER Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Aufgaben Dialogfeld ungefähr alle 200 Millisekunden gesendet.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- Windows-Steuerelemente für TDN_TIMER Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344106"
---
# <a name="tdn_timer-notification-code"></a>TDN-Zeit Geber \_ Benachrichtigungs Code

Wird von einem Aufgaben Dialogfeld ungefähr alle 200 Millisekunden gesendet. Dieser Benachrichtigungs Code wird gesendet, wenn das TDF- \_ Rückruf- \_ Timer-Flag im **dwFlags** -Member der [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) -Struktur festgelegt wurde, die an die [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Funktion übergeben wurde. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der **TaskDialogIndirect** -Methode registriert werden kann.


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **DWORD** , das die Anzahl der Millisekunden seit der Erstellung des Dialog Felds angibt, oder dieser Benachrichtigungs Code hat den Wert " **\_ false**" zurückgegeben.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Zum Zurücksetzen der TickCount-Anwendung muss die Anwendung den Wert " **\_ false**" zurückgeben, andernfalls wird der Wert für "TickCount" weiter erhöht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





