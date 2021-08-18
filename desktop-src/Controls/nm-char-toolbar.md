---
title: NM_CHAR (Symbolleiste) Benachrichtigungscode (Commctrl.h)
description: Wird von einer Symbolleiste gesendet, wenn eine WM \_ CHAR-Nachricht empfangen wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- NM_CHAR -Benachrichtigungscode (Symbolleiste) Windows Steuerelementen
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a318c7385e9d7205ad0fa159e1f987c5d650d27414eefeed4d915c5544cb4564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018938"
---
# <a name="nm_char-toolbar-notification-code"></a>NM \_ CHAR-Benachrichtigungscode (Symbolleiste)

Wird von einer Symbolleiste gesendet, wenn eine [**WM \_ CHAR-Nachricht**](/windows/desktop/inputdev/wm-char) empfangen wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMCHAR-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmchar) die zusätzliche Informationen über das Zeichen enthält, das den Benachrichtigungscode verursacht hat. Das **dwItemPrev-Element** dieser Struktur enthält den Befehlsbezeichner des Elements, das derzeit hot ist, oder -1, wenn derzeit kein Element hot ist. Das **dwItemNext-Element** dieser Struktur enthält den Befehlsbezeichner des Elements, das heiß wird, oder -1, wenn der Schlüssel nicht mit dem Zugriffstaste eines Elements übereinstimmen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** um anzugeben, dass die Symbolleiste das Zeichen nicht verarbeiten soll, und **FALSE,** damit die Symbolleiste das Zeichen verarbeiten soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

