---
title: LVM_GETFOOTERITEM Nachricht (Commctrl.h)
description: Ruft Informationen zu einem Fußzeilenelement in einem Listenansichtssteuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ GetFooterItem-Makros.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- LVM_GETFOOTERITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0b38bb8a91f93c456bd8096a3736eaec79e6c3472d0f18a133de482bb2c0328
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968280"
---
# <a name="lvm_getfooteritem-message"></a>LVM \_ GETFOOTERITEM-Nachricht

Ruft Informationen zu einem Fußzeilenelement in einem Listenansichtssteuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ GetFooterItem-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Der Index des Elements.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**LVFOOTERITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) um einen Wert für die **Zustands-** und/oder **pszText-Member** gemäß dem Wert des **Maskenmembers** zu erhalten. Der aufrufende Prozess ist dafür verantwortlich, diese Struktur zuzuordnen und deren Member so festzulegen, dass sie dem Empfänger angeben, welche Informationen zurückgegeben werden sollen. Weitere Informationen finden Sie unter **LVFOOTERITEM.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





