---
title: TCN_GETOBJECT Benachrichtigungscode (Commctrl.h)
description: Wird von einem Registerkarten-Steuerelement gesendet, wenn es über den erweiterten Stil TCS EX REGISTERDROP verfügt und ein Objekt über ein Registerkartenelement \_ \_ im Steuerelement gezogen wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- TCN_GETOBJECT Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf5ec3a314a7380ccff5f8613145c890f8f304d73289ad5354b8668a09070b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166903"
---
# <a name="tcn_getobject-notification-code"></a>TCN \_ GETOBJECT-Benachrichtigungscode

Wird von einem Registerkarten-Steuerelement gesendet, wenn es über den erweiterten [**Stil TCS \_ EX \_ REGISTERDROP**](tab-control-extended-styles.md) verfügt und ein Objekt über ein Registerkartenelement im Steuerelement gezogen wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMOBJECTNOTIFY-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) die Informationen über das Registerkartenelement enthält, über das das Objekt gezogen wird, und Daten empfängt, die die Anwendung als Antwort auf diese Meldung zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungscode verarbeitet, muss 0 (null) zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





