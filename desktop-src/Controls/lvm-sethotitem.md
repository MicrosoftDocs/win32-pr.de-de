---
title: LVM_SETHOTITEM Meldung (kommstrg. h)
description: Legt das heiße Element für ein Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das ListView-Makro "*" verwenden \_ .
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- Windows-Steuerelemente für LVM_SETHOTITEM Meldung
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c17bc67c530581b79a87030b31b655f856dd0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739944"
---
# <a name="lvm_sethotitem-message"></a>LVM- \_ Nachricht

Legt das heiße Element für ein Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**ListView- \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) Makro "*" verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index des Elements, das als heißes Element festgelegt werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements zurück, das zuvor heiß war.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





