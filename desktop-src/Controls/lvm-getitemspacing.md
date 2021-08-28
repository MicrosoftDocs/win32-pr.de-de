---
title: LVM_GETITEMSPACING Nachricht (Commctrl.h)
description: Bestimmt den Abstand zwischen Elementen in einem Listenansichtssteuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItemSpacing-Makros senden.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- LVM_GETITEMSPACING Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 687a1aa75d71b96cebe855bb97ea57f0a9c628ed49b1ef7a51a7557b23b5ce41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088890"
---
# <a name="lvm_getitemspacing-message"></a>LVM \_ GETITEMSPACING-Nachricht

Bestimmt den Abstand zwischen Elementen in einem Listenansichtssteuerelement. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemSpacing-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ansicht, für die der Elementabstand abgerufen werden soll. Dieser Parameter ist **true** für die kleine Symbolansicht oder **FALSE** für die Symbolansicht.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Abstand zwischen Elementen zurück. Der horizontale Abstand ist im [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthalten, und der vertikale Abstand ist im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

