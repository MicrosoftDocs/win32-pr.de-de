---
title: LVM_SETTEXTCOLOR-Nachricht (Commctrl.h)
description: Legt die Textfarbe eines Listenansicht-Steuerelements fest. Sie können diese Nachricht explizit oder mithilfe des \_ ListView-Makros SetTextColor senden.
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- LVM_SETTEXTCOLOR Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: c70cb9de975440a4093ef8c88992305d294cc04f362c8e9ccb3434937b78f007
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217370"
---
# <a name="lvm_settextcolor-message"></a>LVM \_ SETTEXTCOLOR-Meldung

Legt die Textfarbe eines Listenansicht-Steuerelements fest. Sie können diese Nachricht explizit oder mithilfe des [**\_ ListView-Makros SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein [**COLORREF,**](/windows/desktop/gdi/colorref) das die neue Textfarbe angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

