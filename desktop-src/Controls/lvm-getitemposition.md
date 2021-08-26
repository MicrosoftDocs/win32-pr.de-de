---
title: LVM_GETITEMPOSITION Nachricht (Commctrl.h)
description: Ruft die Position eines Listenansichtselements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItemPosition-Makros senden.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- LVM_GETITEMPOSITION Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d4f4a55f88b6af9828420871de80117ae492bf53c8a62883e43f928c4f5c70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002620"
---
# <a name="lvm_getitemposition-message"></a>LVM \_ GETITEMPOSITION-Nachricht

Ruft die Position eines Listenansichtselements ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemPosition-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index des Listenansichtselements.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf [](/previous-versions//dd162805(v=vs.85)) eine POINT-Struktur, die die Position der oberen linken Ecke des Elements in Ansichtskoordinaten empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

