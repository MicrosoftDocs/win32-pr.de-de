---
title: LVM_SUBITEMHITTEST (Commctrl.h)
description: Bestimmt, welches Listenansichtselement oder Unterelement sich an einer bestimmten Position befindet. Sie können diese Nachricht explizit oder mithilfe des Makros ListView \_ SubItemHitTest senden.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- LVM_SUBITEMHITTEST message Windows Controls
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341f9b3f84646abe975c6543aef802450496154862353b7bbdd1af2c07c087ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830641"
---
# <a name="lvm_subitemhittest-message"></a>LVM \_ SUBITEMHITTEST-Nachricht

Bestimmt, welches Listenansichtselement oder Unterelement sich an einer bestimmten Position befindet. Sie können diese Nachricht explizit oder mithilfe des [**Makros ListView \_ SubItemHitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss den Wert 0 (null) haben. **Windows Vista.** Sollte -1 sein, wenn **das iGroup-Mitglied** von *lParam* abgerufen werden soll.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVHITTESTINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) Die [**POINT-Struktur**](/previous-versions//dd162805(v=vs.85)) in **LVHITTESTINFO** sollte auf die Clientkoordinaten festgelegt werden, die getestet werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des getesteten Elements oder Unterelements zurück, sofern eins vorkommt, andernfalls -1. Wenn sich ein Element oder Unterelement an den angegebenen Koordinaten befindet, werden die Felder der [**LVHITTESTINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) mit den entsprechenden Trefferinformationen gefüllt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

