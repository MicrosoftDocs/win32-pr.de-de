---
title: TDN_VERIFICATION_CLICKED Benachrichtigungscode (Commctrl.h)
description: Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer auf das Kontrollkästchen Überprüfung des Aufgabendialogfelds klickt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: cd7bc07a-9a70-4361-abfa-986a5a2e13e0
keywords:
- TDN_VERIFICATION_CLICKED Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TDN_VERIFICATION_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642d247e95e77c797a5dbd8c2c5ecaf4c9b083261ea848479395f8bb22fa325d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166643"
---
# <a name="tdn_verification_clicked-notification-code"></a>TDN \_ VERIFICATION CLICKED notification code (TDN-ÜBERPRÜFUNG: \_ Benachrichtigungscode, auf den geklickt wurde)

Wird von einem Aufgabendialogfeld gesendet, wenn der Benutzer auf das Kontrollkästchen Überprüfung des Aufgabendialogfelds klickt. Dieser Benachrichtigungscode wird nur über die Rückruffunktion des Aufgabendialogfelds empfangen, die mit der [**TaskDialogIndirect-Methode registriert werden**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) kann.


```C++
TDN_VERIFICATION_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Eine **BOOL,** die den Status des Überprüfungskontrollkästchens angibt. Er ist **TRUE,** wenn das Überprüfungskontrollkästchen aktiviert ist, oder **FALSE,** wenn es deaktiviert ist.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)
</dt> </dl>

 

