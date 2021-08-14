---
title: NM_NCHITTEST Benachrichtigungscode (Rebar) (Commctrl.h)
description: 'NM_NCHITTEST Benachrichtigungscode (Rebar): Wird von einem Rebar-Steuerelement gesendet, wenn das Steuerelement eine WM \_ NCHITTEST-Nachricht empfängt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.'
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- NM_NCHITTEST -Benachrichtigungscode (Rebar) Windows Controls
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
ms.openlocfilehash: b5831ca9dbeda35c7757613cae1d31db921aa80f4b749d4c9407339a2531abcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410701"
---
# <a name="nm_nchittest-rebar-notification-code"></a>NM \_ NCHITTEST-Benachrichtigungscode (Rebar)

Wird von einem Rebar-Steuerelement gesendet, wenn das Steuerelement eine [**WM \_ NCHITTEST-Nachricht**](/windows/desktop/inputdev/wm-nchittest) empfängt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMMOUSE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) die Informationen zum Benachrichtigungscode enthält. Das **dwItemSpec-Member** enthält den Bandindex, über den die Treffertestnachricht aufgetreten ist, und das **pt-Member** enthält die Mauskoordinaten der Treffertestnachricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie 0 (null) zurück, damit die Leiste die Standardverarbeitung der Treffertestnachricht ausführen kann, oder geben Sie einen der unter \* [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) dokumentierten HT-Werte zurück, um die Standardmäßige Treffertestverarbeitung zu überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

