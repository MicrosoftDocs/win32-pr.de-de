---
title: LVN_ITEMACTIVATE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer ein Element aktiviert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- Windows-Steuerelemente für LVN_ITEMACTIVATE Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106665"
---
# <a name="lvn_itemactivate-notification-code"></a>LVN \_ itemaktivierungs-Benachrichtigungs Code

Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer ein Element aktiviert. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

[Version 4,71](common-control-versions.md). Zeiger auf eine [**nmitemaktivierungs**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.

[Version 4,70](common-control-versions.md) und früher. Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung, die diesen Benachrichtigungs Code empfängt, muss NULL zurückgeben.

## <a name="remarks"></a>Bemerkungen

Zum Abrufen der zu aktivierenden Elemente sollte die empfangende Anwendung die [**LVM- \_ getselectedcount**](lvm-getselectedcount.md) -Nachricht verwenden, um die Anzahl der ausgewählten Elemente abzurufen, und dann die [**LVM- \_ GetNextItem**](lvm-getnextitem.md) -Nachricht mit dem **\_ ausgewählten "lvni** " senden, bis alle Elemente abgerufen wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





