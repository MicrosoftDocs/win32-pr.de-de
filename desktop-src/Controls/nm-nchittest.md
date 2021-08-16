---
title: NM_NCHITTEST Benachrichtigungscode (Commctrl.h)
description: 'NM_NCHITTEST Benachrichtigungscode: Wird von einem Steuerelement für die Neuleiste gesendet, wenn das Steuerelement eine \_ WM-NCHITTEST-Nachricht empfängt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.'
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
ms.openlocfilehash: ab16a835e5e321b916f27b6c79141495f3c05cd4ca8e979e77fef50f84e2ca83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410691"
---
# <a name="nm_nchittest-notification-code"></a>NM \_ NCHITTEST-Benachrichtigungscode

Wird von einem Rebar-Steuerelement gesendet, wenn das Steuerelement eine [**WM \_ NCHITTEST-Nachricht empfängt.**](/windows/desktop/inputdev/wm-nchittest) Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMMOUSE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) die Informationen zum Benachrichtigungscode enthält. Das *pt-Element* enthält die Mauskoordinaten der Treffertestmeldung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Sofern nicht anders angegeben, geben Sie 0 (null) zurück, damit das Steuerelement die Standardverarbeitung der Treffertestmeldung durchführen kann, oder geben Sie einen der \* unter [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) dokumentierten HT-Werte zurück, um die Standardmäßige Verarbeitung von Treffertests zu überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

