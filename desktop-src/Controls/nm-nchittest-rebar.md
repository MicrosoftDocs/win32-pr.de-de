---
title: NM_NCHITTEST(Rebar)-Benachrichtigungscode (Commctrl.h)
description: 'NM_NCHITTEST(Rebar)-Benachrichtigungscode: Wird von einem Rebar-Steuerelement gesendet, wenn das Steuerelement eine \_ WM-NCHITTEST-Nachricht empfängt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.'
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- NM_NCHITTEST(Rebar)-Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7935f1b3e990db55518c9d22537e8fb6db97962
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112328"
---
# <a name="nm_nchittest-rebar-notification-code"></a>\_NM-NCHITTEST-Benachrichtigungscode (Rebar)

Wird von einem Rebar-Steuerelement gesendet, wenn das Steuerelement eine [**WM \_ NCHITTEST-Nachricht empfängt.**](/windows/desktop/inputdev/wm-nchittest) Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMMOUSE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) die Informationen zum Benachrichtigungscode enthält. Das **dwItemSpec-Element** enthält den Bandindex, über den die Treffertestmeldung aufgetreten ist, und das **pt-Element** enthält die Mauskoordinaten der Treffertestmeldung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie 0 (null) zurück, damit die Neuleiste die Standardverarbeitung der Treffertestmeldung durchführen kann, oder geben Sie einen der \* unter [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) dokumentierten HT-Werte zurück, um die Standardmäßige Verarbeitung von Treffertests zu überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

