---
title: LVM_SETBKCOLOR Meldung (Commctrl.h)
description: Legt die Hintergrundfarbe eines Listenansicht-Steuerelements fest. Sie können diese Nachricht explizit oder mithilfe des ListView \_ SetBkColor-Makros senden.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- LVM_SETBKCOLOR Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 1b8acfb07a91fae470d893facf6af051397fac2f0d9f4f6990ab4ff67744d8ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391610"
---
# <a name="lvm_setbkcolor-message"></a>LVM \_ SETBKCOLOR-Meldung

Legt die Hintergrundfarbe eines Listenansicht-Steuerelements fest. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetBkColor-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Die festzulegende Hintergrundfarbe oder der CLR \_ NONE-Wert für keine Hintergrundfarbe. Listenansichtssteuerelemente mit Hintergrundfarben zeichnen sich deutlich schneller neu als Steuerelemente ohne Hintergrundfarben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





