---
title: LVM_SETBKCOLOR Meldung (kommstrg. h)
description: Legt die Hintergrundfarbe eines Listenansicht-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des ListView \_ SetBkColor-Makros senden.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- Windows-Steuerelemente für LVM_SETBKCOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956720"
---
# <a name="lvm_setbkcolor-message"></a>LVM- \_ SetBkColor-Nachricht

Legt die Hintergrundfarbe eines Listenansicht-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Die festzulegende Hintergrundfarbe oder der CLR \_ None-Wert für keine Hintergrundfarbe. Listenansicht-Steuerelemente mit Hintergrundfarben zeichnen sich deutlich schneller aus als solche ohne Hintergrundfarben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





