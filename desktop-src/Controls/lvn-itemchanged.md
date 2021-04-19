---
title: LVN_ITEMCHANGED Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass sich ein Element geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: d5f0b4e7-0d0c-4021-942b-71fd31880599
keywords:
- Windows-Steuerelemente für LVN_ITEMCHANGED Benachrichtigungs
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
ms.openlocfilehash: c856292e9b94590b50593a6c3c5f145497f47f28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345942"
---
# <a name="lvn_itemchanged-notification-code"></a>LVN \_ ItemChanged-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass sich ein Element geändert hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_ITEMCHANGED

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) -Struktur, die das Element identifiziert und angibt, welche seiner Attribute geändert wurden. Wenn der **iItem** -Member der Struktur, auf die von *LPARAM* verwiesen wird,-1 ist, wurde die Änderung auf alle Elemente in der Listenansicht angewendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn ein Listenansicht-Steuerelement den [**LVS \_**](list-view-window-styles.md) -Besitzer Daten Stil hat und der Benutzer einen Bereich von Elementen auswählt, indem er die UMSCHALTTASTE gedrückt hält und auf die Maus klickt, werden LVN \_ ItemChanged-Benachrichtigungs Codes nicht für jedes ausgewählte oder ausgewählte Element gesendet. Stattdessen erhalten Sie einen einzelnen [LVN- \_ odstatechanged](lvn-odstatechanged.md) -Benachrichtigungs Code, der angibt, dass sich der Zustand eines Bereichs von Elementen geändert hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





