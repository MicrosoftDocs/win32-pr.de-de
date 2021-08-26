---
title: TVM_SETITEM Meldung (Commctrl.h)
description: Die TVM \_ SETITEM-Nachricht legt einige oder alle Attribute eines Strukturansichtselements fest. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetItem-Makros senden.
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- TVM_SETITEM Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 9521bc67766dbb503fc205e966d6ce72e674a4050b6c0d237c885dcb4a8f4b68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913940"
---
# <a name="tvm_setitem-message"></a>TVM \_ SETITEM-Nachricht

Die **TVM \_ SETITEM-Nachricht** legt einige oder alle Attribute eines Strukturansichtselements fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetItem-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tvitema) die die neuen Elementattribute enthält. Ab [Version 4.71](common-control-versions.md) können Sie stattdessen eine [**TVITEMEX-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Das **hItem-Element** der [**TVITEM-**](/windows/win32/api/commctrl/ns-commctrl-tvitema) oder [**TVITEMEX-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifiziert das Element, und der **Maskenmember** gibt an, welche Attribute festgelegt werden sollen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVM \_ SETITEMW** (Unicode) und **TVM \_ SETITEMA** (ANSI)<br/>                   |



 

 





