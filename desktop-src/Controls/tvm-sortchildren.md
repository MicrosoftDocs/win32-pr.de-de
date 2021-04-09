---
title: TVM_SORTCHILDREN Meldung (kommstrg. h)
description: Sortiert die untergeordneten Elemente des angegebenen übergeordneten Elements in einem Strukturansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SortChildren-Makros senden.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- Windows-Steuerelemente für TVM_SORTCHILDREN Meldung
topic_type:
- apiref
api_name:
- TVM_SORTCHILDREN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341591c31accb4aab0b49f611359a93ec99c0cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040941"
---
# <a name="tvm_sortchildren-message"></a>TVM \_ SortChildren-Meldung

Sortiert die untergeordneten Elemente des angegebenen übergeordneten Elements in einem Strukturansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SortChildren**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Wert, der angibt, ob die Sortierung rekursiv ist. Legen Sie " *wParam* " auf " **true** " fest, um alle Ebenen von untergeordneten Elementen unterhalb des übergeordneten Elements Andernfalls werden nur die unmittelbar untergeordneten Elemente des übergeordneten Elements sortiert.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das übergeordnete Element, dessen untergeordnete Elemente sortiert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

In dieser Meldung werden die Strukturelemente mithilfe von [**lstrincmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) auf dem Elementnamen alphabetisch sortiert. Mit der [**TVM \_ SortChildren**](tvm-sortchildrencb.md) -Nachricht können Sie das Bestellverhalten anpassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

