---
title: NM_NCHITTEST Benachrichtigungscode (Commctrl.h)
description: 'NM_NCHITTEST Benachrichtigungscode: Wird von einem Rebar-Steuerelement gesendet, wenn das Steuerelement eine WM \_ NCHITTEST-Nachricht empfängt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.'
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST Benachrichtigungscode Windows-Steuerelemente
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
ms.openlocfilehash: 68ede0ac017fbe5146cd68e51e2a38c7f66c7898
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112318"
---
# <a name="nm_nchittest-notification-code"></a>NM \_ NCHITTEST-Benachrichtigungscode

Wird von einem Rebar-Steuerelement gesendet, wenn das Steuerelement eine [**WM \_ NCHITTEST-Nachricht**](/windows/desktop/inputdev/wm-nchittest) empfängt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMMOUSE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) die Informationen zum Benachrichtigungscode enthält. Das *pt-Member* enthält die Mauskoordinaten der Treffertestnachricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie , sofern nicht anders angegeben, 0 (null) zurück, damit das Steuerelement die Standardverarbeitung der Treffertestnachricht ausführen kann, oder geben Sie einen der unter \* [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) dokumentierten HT-Werte zurück, um die Standardmäßige Treffertestverarbeitung zu überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

