---
title: IPN_FIELDCHANGED Benachrichtigungs Code (kommctrl. h)
description: Wird gesendet, wenn der Benutzer ein Feld im Steuerelement ändert oder von einem Feld zu einem anderen verschoben wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- Windows-Steuerelemente für IPN_FIELDCHANGED Benachrichtigungs
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
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040855"
---
# <a name="ipn_fieldchanged-notification-code"></a>IPN \_ FieldChanged-Benachrichtigungs Code

Wird gesendet, wenn der Benutzer ein Feld im Steuerelement ändert oder von einem Feld zu einem anderen verschoben wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmipaddress**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) -Struktur, die Informationen über die geänderte Adresse enthält. Der **iValue** -Member dieser Struktur enthält den eingegebenen Wert, auch wenn er außerhalb des Bereichs des Felds liegt. Sie können dieses Element in einen beliebigen Wert ändern, der als Reaktion auf diesen Benachrichtigungs Code innerhalb des Bereichs für das Feld liegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Dieser Benachrichtigungs Code wird nicht als Antwort auf eine [**IPM- \_ setAddress**](ipm-setaddress.md) -Nachricht gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





