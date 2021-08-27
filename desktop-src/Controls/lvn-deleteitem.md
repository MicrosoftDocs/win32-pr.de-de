---
title: LVN_DELETEITEM Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansichtssteuerelements, dass ein Element gelöscht werden soll. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- LVN_DELETEITEM Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5637cf2e8de98c056635cef2e68a7672f52b649c0162920f647384a2ceb4e64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062160"
---
# <a name="lvn_deleteitem-notification-code"></a>LVN \_ DELETEITEM-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Listenansichtssteuerelements, dass ein Element gelöscht werden soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLISTVIEW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) Das **iItem-Element** identifiziert das element, das gelöscht wird. Wenn das Steuerelement nicht über den **LVS \_ OWNERDATA-Stil** verfügt, ist *lParam* die anwendungsdefinierten Daten, die dem Element zugeordnet sind. Alle anderen Member dieser -Struktur sind 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Fügen Sie der Listenansicht während der Verarbeitung dieses Benachrichtigungscodes keine Elemente hinzu, löschen oder neu anordnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





