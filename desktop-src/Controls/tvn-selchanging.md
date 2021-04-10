---
title: TVN_SELCHANGING Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Baumansicht-Steuer Elements, dass sich die Auswahl von einem Element in ein anderes ändert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- Windows-Steuerelemente für TVN_SELCHANGING Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040496"
---
# <a name="tvn_selchanging-notification-code"></a>TVN \_ selchanging-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Baumansicht-Steuer Elements, dass sich die Auswahl von einem Element in ein anderes ändert. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur. Die Member **itemold** und **itemnew** enthalten gültige Informationen über das aktuell ausgewählte Element und das neu ausgewählte Element. Der **Aktionsmember** gibt an, ob eine Maus-oder Tastatur Aktion eine Änderung der Auswahl bewirkt. Eine Liste der möglichen Werte finden Sie in der Beschreibung des von der [TVN \_ selchanged](tvn-selchanged.md) -Benachrichtigungs Codes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, um zu verhindern, dass sich die Auswahl ändert.

## <a name="remarks"></a>Bemerkungen

Bei der Reaktion auf diesen Benachrichtigungs Code sollten Anwendungen die Elemente, die die Auswahl erhalten oder verlieren, nicht löschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ Selchangingw** (Unicode) und **TVN \_ selchanginga** (ANSI)<br/>           |



 

 





