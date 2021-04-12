---
title: LVN_COLUMNDROPDOWN Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn die Dropdown-Schaltfläche der Listenansicht gedrückt wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 752d745e-4482-425c-af3c-f9707cbb03d7
keywords:
- Windows-Steuerelemente für LVN_COLUMNDROPDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_COLUMNDROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792d29268548d95a7f3e70b05d9d2de368a03cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517789"
---
# <a name="lvn_columndropdown-notification-code"></a>LVN- \_ columndropdown-Benachrichtigungs Code

Wird von einem Listenansicht-Steuerelement gesendet, wenn die Dropdown-Schaltfläche der Listenansicht gedrückt wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_COLUMNDROPDOWN
        
    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur, die den Benachrichtigungs Code beschreibt. Der Aufrufer ist dafür verantwortlich, diese Struktur zuzuordnen, einschließlich der enthaltenen [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur. Legen Sie die Member der **NMHDR** -Struktur fest. Das **Codemember** muss auf LVN \_ columndropdown festgelegt werden.

Legen Sie den **iItem** -Member der [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur auf-1 fest. Legen Sie den **iSubItem** -Member auf den Index des unter Elements fest. Legen Sie die Member **unewstate**, **uoldstate** und **LPARAM** auf NULL fest. Die übrigen Member der **NMLISTVIEW** -Struktur werden nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Der Benachrichtigungs Empfänger wandelt *LPARAM* ein, um die [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur abzurufen. Der *wParam* -Parameter enthält die ID des Steuer Elements, das den Benachrichtigungs Code sendet.

Wenn ein Header Steuerelement ein untergeordnetes Element der Listenansicht ist, sollte das Header Steuerelement diesen Benachrichtigungs Code an das Listenansicht-Steuerelement senden, wenn das Header Steuerelement den [Hdn- \_ Dropdown](hdn-dropdown.md) -Benachrichtigungs Code empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





