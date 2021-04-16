---
title: LVN_LINKCLICK Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass auf einen Link geklickt wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: de8f40d6-b79e-4324-af67-9a3c0915609d
keywords:
- Windows-Steuerelemente für LVN_LINKCLICK Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd69fb463e71523fcbd4eeb65a6a718d27847c09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479431"
---
# <a name="lvn_linkclick-notification-code"></a>LVN \_ linkclick-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass auf einen Link geklickt wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_LINKCLICK
        
    pLinkInfo = (NMLVLINK*) lParam;         
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) -Struktur. Der Bezeichner der Gruppe, die den Link enthält, befindet sich im **iSubItem** -Member.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Das folgende Beispiel zeigt, wie eine Anwendung in Ihrem [**WM \_**](wm-notify.md) -Benachrichtigungs Meldungs Handler auf diesen Benachrichtigungs Code reagieren könnte. Im Beispiel wird der reduzierte Status der Gruppe gewechselt und der entsprechende Linktext festgelegt.

``` syntax
case LVN_LINKCLICK:
{
    NMLVLINK* pLinkInfo = (NMLVLINK*)lParam;
    HWND hList = pLinkInfo->hdr.hwndFrom;
    LVGROUP groupInfo;
    groupInfo.cbSize = sizeof(groupInfo);
    groupInfo.mask = LVGF_TASK;
    int groupIndex = pLinkInfo->iSubItem;
    if (ListView_GetGroupState(hList, groupIndex, LVGS_COLLAPSED))
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, 0);
        groupInfo.pszTask = L"Hide";
    }
    else
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, LVGS_COLLAPSED);
        groupInfo.pszTask = L"Show";
     }
      ListView_SetGroupInfo(hList, groupIndex, &groupInfo);
      break;
}
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





