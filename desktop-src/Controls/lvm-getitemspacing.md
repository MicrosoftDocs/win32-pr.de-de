---
title: LVM_GETITEMSPACING Meldung (kommstrg. h)
description: Bestimmt den Abstand zwischen Elementen in einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getitemspacing-Makros senden.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- Windows-Steuerelemente für LVM_GETITEMSPACING Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956990"
---
# <a name="lvm_getitemspacing-message"></a>LVM- \_ getitemspacing-Nachricht

Bestimmt den Abstand zwischen Elementen in einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getitemspacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Ansicht, für die die Element Abstände abgerufen werden sollen. Dieser Parameter ist für die kleine Symbol Ansicht **true** , oder für die Symbol Ansicht ist der Wert **false** .

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Abstand zwischen Elementen zurück. Der horizontale Abstand ist im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthalten, und der vertikale Abstand ist im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

