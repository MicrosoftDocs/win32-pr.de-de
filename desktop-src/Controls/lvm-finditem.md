---
title: LVM_FINDITEM Meldung (kommstrg. h)
description: Sucht nach einem Listen Ansichts Element mit den angegebenen Merkmalen. Sie können diese Nachricht explizit oder mithilfe des ListView \_ FindItem-Makros senden.
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- Windows-Steuerelemente für LVM_FINDITEM Meldung
topic_type:
- apiref
api_name:
- LVM_FINDITEM
- LVM_FINDITEMA
- LVM_FINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f7dfc19e263a6ab7ad29b5e514fa4e52c1a9ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475186"
---
# <a name="lvm_finditem-message"></a>LVM- \_ FindItem-Nachricht

Sucht nach einem Listen Ansichts Element mit den angegebenen Merkmalen. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements, mit dem mit der Suche begonnen werden soll, oder-1, um von Anfang an zu beginnen. Das angegebene Element ist selbst von der Suche ausgeschlossen.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) -Struktur, die Informationen darüber enthält, nach welchen Informationen gesucht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements zurück, wenn erfolgreich, andernfalls-1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ Finditemw** (Unicode) und **LVM \_ finditema** (ANSI)<br/>                 |



 

 





