---
title: TVM_GETITEM Meldung (kommstrg. h)
description: Ruft einige oder alle der Attribute eines Struktur Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ Makros "GetItem" senden.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- Windows-Steuerelemente für TVM_GETITEM Meldung
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106574"
---
# <a name="tvm_getitem-message"></a>TVM- \_ GetItem-Meldung

Ruft einige oder alle der Attribute eines Struktur Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Makros " \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -Struktur, die die Informationen angibt, die abgerufen werden sollen, und Informationen über das Element empfängt. Mit [Version 4,71](common-control-versions.md) und höher können Sie stattdessen eine [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) -Struktur verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn die Nachricht gesendet wird, identifiziert das **Hitem** -Element der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -oder [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) -Struktur das Element, über das Informationen abgerufen werden sollen, und der **Mask** -Member gibt die abzurufenden Attribute an.

Wenn das tvif- \_ textflag im **Mask** -Member der [**tvitem**](/windows/win32/api/commctrl/ns-commctrl-tvitema) -oder [**tvitemex**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) -Struktur festgelegt ist, muss der **pszText** -Member auf einen gültigen Puffer zeigen, und das **cchtextmax** -Element muss auf die Anzahl der Zeichen in diesem Puffer festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVM \_ Getitemw** (Unicode) und **TVM \_ getitema** (ANSI)<br/>                   |



 

 





