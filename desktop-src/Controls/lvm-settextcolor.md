---
title: LVM_SETTEXTCOLOR Meldung (kommstrg. h)
description: Legt die Textfarbe eines Listenansicht-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des ListView \_ SetTextColor-Makros senden.
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- Windows-Steuerelemente für LVM_SETTEXTCOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b30c965bd523cd5638c894b47fc4785ffbdd09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103355"
---
# <a name="lvm_settextcolor-message"></a>LVM- \_ SetTextColor-Meldung

Legt die Textfarbe eines Listenansicht-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein [**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue Textfarbe angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

