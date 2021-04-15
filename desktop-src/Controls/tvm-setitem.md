---
title: TVM_SETITEM Meldung (kommstrg. h)
description: Mit der TVM \_ SetItem-Meldung werden einige oder alle der Attribute eines Struktur Ansichts Elements festgelegt. Sie können diese Nachricht explizit oder mithilfe des TreeView-Makros (TreeView) senden \_ .
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- Windows-Steuerelemente für TVM_SETITEM Meldung
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95750af3aa43a25f0ff4eae5533df5d9aef23537
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476950"
---
# <a name="tvm_setitem-message"></a>TVM-nach \_ richten-Nachricht

Mit der **TVM \_ SetItem** -Meldung werden einige oder alle der Attribute eines Struktur Ansichts Elements festgelegt. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ -Makros (TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) ) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die die neuen Element Attribute enthält. Mit [Version 4,71](common-control-versions.md) und höher können Sie stattdessen eine [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) -Struktur verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Das **Hitem** -Element der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -oder [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) -Struktur identifiziert das Element, und der **Mask** -Member gibt an, welche Attribute festgelegt werden sollen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVM \_** "S" (Unicode) und " **TVM \_** " (ANSI)<br/>                   |



 

 





