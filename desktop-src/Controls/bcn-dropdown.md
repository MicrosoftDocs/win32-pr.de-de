---
title: BCN_DROPDOWN Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn der Benutzer auf einen Dropdown Pfeil auf einer Schaltfläche klickt. Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: 61503b8d-193e-4855-b9eb-35c0dc636c02
keywords:
- Windows-Steuerelemente für BCN_DROPDOWN Benachrichtigungs
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
ms.openlocfilehash: e78512419f62beaa82aff42ccaf951d34130fe3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338137"
---
# <a name="bcn_dropdown-notification-code"></a>BCN- \_ Dropdown-Benachrichtigungs Code

Wird gesendet, wenn der Benutzer auf einen Dropdown Pfeil auf einer Schaltfläche klickt. Das übergeordnete Fenster des Steuer Elements empfängt diesen Benachrichtigungs Code in Form einer [**WM \_**](wm-notify.md) -Benachrichtigungs Meldung.


```C++
BCN_DROPDOWN
        
    pnmdropdown = (NMBCDROPDOWN*) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmbcdropdown**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) -Struktur. Der **rcbutton** -Member wird so festgelegt, dass der Dropdown Bereich beschrieben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Der Benachrichtigungs Empfänger wandelt **LPARAM** ein, um die [**nmbcdropdown**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown) -Struktur abzurufen. **WParam** enthält die ID des Steuer Elements, das diese Nachricht sendet. Das Schaltflächen-Steuerelement muss einen Dropdown-Schaltflächen Stil aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

 





