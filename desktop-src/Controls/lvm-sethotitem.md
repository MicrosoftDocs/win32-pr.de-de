---
title: LVM_SETHOTITEM Meldung (Commctrl.h)
description: Legt das heiße Element für ein Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das \_ ListView-Makro SetHotItem verwenden.
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- LVM_SETHOTITEM Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 6937cbed8150bf14eb71e167b8ed54d6f6b47ae995a3af989613cba30c7ca3fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077240"
---
# <a name="lvm_sethotitem-message"></a>LVM \_ SETHOTITEM-Nachricht

Legt das heiße Element für ein Listenansicht-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**\_ ListView-Makro SetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des Elements, das als heißes Element festgelegt werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des Elements zurück, das zuvor heiß war.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





