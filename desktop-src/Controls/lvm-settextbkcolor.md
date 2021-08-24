---
title: LVM_SETTEXTBKCOLOR-Nachricht (Commctrl.h)
description: Legt die Hintergrundfarbe von Text in einem Listenansichtssteuerelement fest. Sie können diese Nachricht explizit oder mithilfe des \_ ListView-Makros SetTextBkColor senden.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- LVM_SETTEXTBKCOLOR Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d9acdc193609f39fb81aa88263724a507695f15dcb8ba0c789df5c2a4f4d128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656230"
---
# <a name="lvm_settextbkcolor-message"></a>LVM \_ SETTEXTBKCOLOR-Nachricht

Legt die Hintergrundfarbe von Text in einem Listenansichtssteuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**\_ ListView-Makros SetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Neue Texthintergrundfarbe. Dies kann CLR \_ NONE ohne Hintergrundfarbe sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





