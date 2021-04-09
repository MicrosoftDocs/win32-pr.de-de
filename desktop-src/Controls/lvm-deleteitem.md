---
title: LVM_DELETEITEM Meldung (kommstrg. h)
description: Entfernt ein Element aus einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView \_ DeleteItem-Makros senden.
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- Windows-Steuerelemente für LVM_DELETEITEM Meldung
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19fce5afbbaa6702f296df12acf7dad4edac16fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102903"
---
# <a name="lvm_deleteitem-message"></a>LVM \_ DeleteItem-Meldung

Entfernt ein Element aus einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des zu löschenden Listen Ansichts Elements.

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



 

 





