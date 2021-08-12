---
title: BCN_DROPDOWN Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn der Benutzer auf einen Dropdownpfeil auf einer Schaltfläche klickt. Das übergeordnete Fenster des Steuerelements empfängt diesen Benachrichtigungscode in Form einer WM \_ NOTIFY-Nachricht.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- BCN_DROPDOWN Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- BCN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbacf22cdabbac7c5d2932c604fab634dbc185207acda8cee311d434478e5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674972"
---
# <a name="bcn_dropdown-notification-code"></a>\_BCN-DROPDOWN-Benachrichtigungscode

Wird gesendet, wenn der Benutzer auf einen Dropdownpfeil auf einer Schaltfläche klickt. Das übergeordnete Fenster des Steuerelements empfängt diesen Benachrichtigungscode in Form einer [**WM \_ NOTIFY-Nachricht.**](wm-notify.md)


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMBCDROPDOWN-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) Der **rcButton-Member** ist so festgelegt, dass er den Dropdownbereich beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Der Benachrichtigungsempfänger castiert **LPARAM,** um die [**NMBCDROPDOWN-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) abzurufen. **WPARAM** enthält die ID des Steuerelements, das diese Nachricht sendet. Das Schaltflächen-Steuerelement muss ein Dropdown-Schaltflächenformat haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



 

 





