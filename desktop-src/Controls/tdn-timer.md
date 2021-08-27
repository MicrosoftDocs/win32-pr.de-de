---
title: TDN_TIMER Benachrichtigungscode (Commctrl.h)
description: Wird von einem Aufgabendialogfeld ungefähr alle 200 Millisekunden gesendet.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER Benachrichtigungscode Windows-Steuerelemente
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
ms.openlocfilehash: eaf3f5d72ef8267c6600decf070875b2dd109114f910d09a5ca343f8fde44005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104450"
---
# <a name="tdn_timer-notification-code"></a>\_TDN-TIMER-Benachrichtigungscode

Wird von einem Aufgabendialogfeld ungefähr alle 200 Millisekunden gesendet. Dieser Benachrichtigungscode wird gesendet, wenn das TDF \_ CALLBACK \_ TIMER-Flag im **dwFlags-Member** der [**TASKDIALOGCONFIG-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) festgelegt wurde, der an die [**TaskDialogIndirect-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) übergeben wurde. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der **TaskDialogIndirect-Methode** registriert werden kann.


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **DWORD,** das die Anzahl von Millisekunden seit der Erstellung des Dialogfelds angibt, oder dieser Benachrichtigungscode hat **S \_ FALSE** zurückgegeben.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Um den Tickcount zurückzusetzen, muss die Anwendung **S \_ FALSE** zurückgeben, andernfalls wird der Tickcount weiter erhöht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





