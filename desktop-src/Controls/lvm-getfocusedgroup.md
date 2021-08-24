---
title: LVM_GETFOCUSEDGROUP Nachricht (Commctrl.h)
description: Ruft die Gruppe ab, die den Fokus besitzt. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ GetFocusedGroup-Makros.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- LVM_GETFOCUSEDGROUP Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETFOCUSEDGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9b253405683c058518706e92e62f09041ae4db0e4bee426aa653103bda2188c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877430"
---
# <a name="lvm_getfocusedgroup-message"></a>LVM \_ GETFOCUSEDGROUP-Nachricht

Ruft die Gruppe ab, die den Fokus besitzt. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ GetFocusedGroup-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index der Gruppe mit dem Status LVGS \_ FOCUSED oder -1 zurück, wenn keine Gruppe mit dem Status LVGS FOCUSED vorhanden \_ ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





