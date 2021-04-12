---
title: LVM_GETFOCUSEDGROUP Meldung (kommstrg. h)
description: Ruft die Gruppe ab, die den Fokus besitzt. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getfocusedgroup-Makros.
ms.assetid: c1902f35-84b7-4f46-89a6-e48148f06172
keywords:
- Windows-Steuerelemente für LVM_GETFOCUSEDGROUP Meldung
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
ms.openlocfilehash: 3e0d12eb637ec1a421a5eaff58636df7bef8f449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475165"
---
# <a name="lvm_getfocusedgroup-message"></a>LVM \_ getfocusedgroup-Meldung

Ruft die Gruppe ab, die den Fokus besitzt. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getfocusedgroup**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfocusedgroup) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index der Gruppe mit dem Status "mit \_ Fokus" oder "-1" zurück, wenn keine Gruppe mit dem Status "lvgs" fokussiert ist \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





