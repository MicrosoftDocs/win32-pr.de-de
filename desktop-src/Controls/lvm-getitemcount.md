---
title: LVM_GETITEMCOUNT (Commctrl.h)
description: Ruft die Anzahl der Elemente in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItemCount-Makros senden.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- LVM_GETITEMCOUNT von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- LVM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1561e893930e4e3eca8de628c1df555e63794c3463edf81af798c53d873c8a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109620"
---
# <a name="lvm_getitemcount-message"></a>LVM \_ GETITEMCOUNT-Nachricht

Ruft die Anzahl der Elemente in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemCount-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Elemente zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





