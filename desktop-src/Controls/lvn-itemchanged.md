---
title: LVN_ITEMCHANGED Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansichtssteuerelements, dass sich ein Element geändert hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- LVN_ITEMCHANGED Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea129a1b62b442b0fb545f29a57e9eab0d6d1bae057996df5bc269d9a4296d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830384"
---
# <a name="lvn_itemchanged-notification-code"></a>LVN \_ ITEMCHANGED-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Listenansichtssteuerelements, dass sich ein Element geändert hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLISTVIEW-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) die das Element identifiziert und angibt, welches seiner Attribute sich geändert hat. Wenn das **iItem-Member** der -Struktur, auf das *lParam* zeigt, -1 ist, wurde die Änderung auf alle Elemente in der Listenansicht angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn ein Listenansicht-Steuerelement den [**LVS \_ OWNERDATA-Stil**](list-view-window-styles.md) auflistet und der Benutzer einen Bereich von Elementen auswählt, indem er die UMSCHALTTASTE gedrückt hält und mit der Maus klickt, werden LVN ITEMCHANGED-Benachrichtigungscodes nicht für jedes ausgewählte oder deaktivierte Element \_ gesendet. Stattdessen erhalten Sie einen einzelnen [LVN \_ ODSTATECHANGED-Benachrichtigungscode,](lvn-odstatechanged.md) der angibt, dass ein Bereich von Elementen den Zustand geändert hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





