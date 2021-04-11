---
title: LVN_ODFINDITEM Meldung (kommstrg. h)
description: Wird von einem Virtual List-View-Steuerelement gesendet, wenn der Besitzer ein bestimmtes Rückruf Element finden muss.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- Windows-Steuerelemente für LVN_ODFINDITEM Meldung
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104811"
---
# <a name="lvn_odfinditem-message"></a>LVN \_ odfinditem-Meldung

Wird von einem [Virtual List-View-](list-view-controls-overview.md) Steuerelement gesendet, wenn der Besitzer ein bestimmtes Rückruf Element finden muss. Beispielsweise sendet das Steuerelement diesen Benachrichtigungs Code, wenn er Tastatureingaben empfängt oder eine [**LVM- \_ FindItem**](lvm-finditem.md) -Nachricht empfängt. Der LVN \_ odfinditem-Benachrichtigungs Code wird in Form einer [**WM- \_**](wm-notify.md) Benachrichtigungs Meldung gesendet.


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmlvfinditem**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) -Struktur, die Informationen enthält, die für die Suche verwendet werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des gefundenen Elements zurück, oder-1, wenn kein Element gefunden wird.

## <a name="remarks"></a>Bemerkungen

Suchinformationen werden in Form einer " [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) "-Struktur gesendet, die ein Member der [**nmlvfinditem**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) -Struktur ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVN \_ Odfinditemw** (Unicode) und **LVN \_ odfinditema** (ANSI)<br/>             |



 

 





