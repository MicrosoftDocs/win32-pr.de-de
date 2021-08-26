---
title: LVM_UPDATE (Commctrl.h)
description: Aktualisiert ein Listenansichtselement. Wenn das Listenansicht-Steuerelement über den LVS AUTOARRANGE-Stil verfügt, bewirkt dieses Makro, dass das \_ Listenansicht-Steuerelement angeordnet wird. Sie können diese Nachricht explizit oder mithilfe des ListView \_ Update-Makros senden.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- LVM_UPDATE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff9067d6eb80c5db7880ee9331a04e9259e9c841ccfe7dd80158a2afbcd06c99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915230"
---
# <a name="lvm_update-message"></a>LVM \_ UPDATE-Nachricht

Aktualisiert ein Listenansichtselement. Wenn das Listenansicht-Steuerelement über den [**LVS \_ AUTOARRANGE-Stil**](list-view-window-styles.md) verfügt, bewirkt dieses Makro, dass das Listenansicht-Steuerelement angeordnet wird. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ Update-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des zu aktualisierenden Elements.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





