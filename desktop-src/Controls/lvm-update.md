---
title: LVM_UPDATE Meldung (kommstrg. h)
description: Aktualisiert ein Listen Ansichts Element. Wenn das Listenansicht-Steuerelement den LVS \_ AutoArrange-Stil hat, bewirkt dieses Makro, dass das Listenansicht-Steuerelement angeordnet ist. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Update Makros senden.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- Windows-Steuerelemente für LVM_UPDATE Meldung
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
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858680"
---
# <a name="lvm_update-message"></a>LVM- \_ Aktualisierungs Meldung

Aktualisiert ein Listen Ansichts Element. Wenn das Listenansicht-Steuerelement den [**LVS \_ AutoArrange**](list-view-window-styles.md) -Stil hat, bewirkt dieses Makro, dass das Listenansicht-Steuerelement angeordnet ist. Sie können diese Nachricht explizit oder mithilfe des [**ListView- \_ Update**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des zu aktualisierenden Elements.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





