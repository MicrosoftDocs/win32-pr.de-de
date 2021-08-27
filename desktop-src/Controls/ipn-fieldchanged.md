---
title: IPN_FIELDCHANGED Benachrichtigungscode (Commctrl.h)
description: Wird gesendet, wenn der Benutzer ein Feld im Steuerelement ändert oder von einem Feld in ein anderes wechselt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467cf7f14f3ff8d62f85d973e9a9d11c4dc6d20488ad5b7e30b4c0787b4b1a6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085550"
---
# <a name="ipn_fieldchanged-notification-code"></a>IPN \_ FIELDCHANGED-Benachrichtigungscode

Wird gesendet, wenn der Benutzer ein Feld im Steuerelement ändert oder von einem Feld in ein anderes wechselt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMIPADDRESS-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) die Informationen über die geänderte Adresse enthält. Der **iValue-Member** dieser Struktur enthält den eingegebenen Wert, auch wenn er sich nicht im Bereich des Felds befindet. Sie können diesen Member in einen beliebigen Wert ändern, der innerhalb des Bereichs für das Feld als Reaktion auf diesen Benachrichtigungscode liegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Dieser Benachrichtigungscode wird nicht als Antwort auf eine [**\_ IPM-SETADDRESS-Nachricht**](ipm-setaddress.md) gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





