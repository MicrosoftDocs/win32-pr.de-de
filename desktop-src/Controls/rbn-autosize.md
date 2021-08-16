---
title: RBN_AUTOSIZE Benachrichtigungscode (Commctrl.h)
description: Wird von einem Rebar-Steuerelement gesendet, das mit dem RBS AUTOIZE-Stil erstellt wurde, wenn die Größe der Leiste automatisch \_ selbst geändert wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- RBN_AUTOSIZE Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32c0ef601562c6887e05c78c06a66cf61e330843769eb3bb66105eb941e09339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985370"
---
# <a name="rbn_autosize-notification-code"></a>RBN \_ AUTOIZE-Benachrichtigungscode

Wird von einem Rebar-Steuerelement gesendet, das mit dem [**RBS \_ AUTOIZE-Stil**](rebar-control-styles.md) erstellt wurde, wenn die Größe der Leiste automatisch selbst geändert wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMRBAUTOSIZE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) die Informationen zum Größenvergrößerungsvorgang enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





