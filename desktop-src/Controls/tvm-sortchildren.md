---
title: TVM_SORTCHILDREN (Commctrl.h)
description: Sortiert die untergeordneten Elemente des angegebenen übergeordneten Elements in einem Strukturansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SortChildren-Makros senden.
ms.assetid: c18bcd5f-c083-46ee-873b-d3100b0d7b04
keywords:
- TVM_SORTCHILDREN von Windows-Steuerelementen
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
ms.openlocfilehash: f975814fadc5271c562e4e8e420c35dbb3450142bed797af83af73fdf81a55d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913800"
---
# <a name="tvm_sortchildren-message"></a>TVM \_ SORTCHILDREN-Meldung

Sortiert die untergeordneten Elemente des angegebenen übergeordneten Elements in einem Strukturansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SortChildren-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Wert, der angibt, ob die Sortierung rekursiv ist. Legen *Sie wParam auf* TRUE **fest,** um alle Ebenen untergeordneter Elemente unterhalb des übergeordneten Elements zu sortieren. Andernfalls werden nur die unmittelbaren übergeordneten unteren Klammern sortiert.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das übergeordnete Element, dessen untergeordnete Elemente sortiert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Meldung alphabetisiert die Strukturelemente [**mithilfe von lstrcmpi**](/windows/desktop/api/winbase/nf-winbase-lstrcmpia) für den Elementnamen. Sie können die [**TVM \_ SORTCHILDRENCB-Nachricht**](tvm-sortchildrencb.md) verwenden, um das Sortierverhalten anzupassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

