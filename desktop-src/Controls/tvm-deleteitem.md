---
title: TVM_DELETEITEM Meldung (Commctrl.h)
description: Entfernt ein Element und alle untergeordneten Elemente aus einem Strukturansichtssteuerelement. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ DeleteItem-Makros senden.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- TVM_DELETEITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef0165ffaf1f0f04b32cda43e21c97fed012ad6d61b32f8919612f8924f7c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018688"
---
# <a name="tvm_deleteitem-message"></a>TVM \_ DELETEITEM-Nachricht

Entfernt ein Element und alle untergeordneten Elemente aus einem Strukturansichtssteuerelement. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ DeleteItem-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

**HTREEITEM-Handle** für das zu löschende Element. Wenn *lParam* auf TVI ROOT oder NULL festgelegt \_ ist, werden alle Elemente gelöscht.  Sie können auch das [**TreeView \_ DeleteAllItems-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) verwenden, um alle Elemente zu löschen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Es ist nicht sicher, Elemente als Reaktion auf eine Benachrichtigung wie [TVN \_ SELCHANGING](tvn-selchanging.md)zu löschen.

Nachdem ein Element gelöscht wurde, ist sein Handle ungültig und kann nicht mehr verwendet werden.

Das übergeordnete Fenster empfängt einen [TVN DELETEITEM-Benachrichtigungscode, \_ ](tvn-deleteitem.md) wenn jedes Element entfernt wird.

Wenn die Elementbezeichnung bearbeitet wird, wird der Bearbeitungsvorgang abgebrochen, und das übergeordnete Fenster empfängt den [TVN \_ ENDLABELEDIT-Benachrichtigungscode.](tvn-endlabeledit.md)

Wenn Sie alle Elemente in einem Strukturansichtssteuerelement mit dem [**TVS \_ NOSCROLL-Stil**](tree-view-control-window-styles.md) löschen, werden elemente, die anschließend hinzugefügt werden, möglicherweise nicht ordnungsgemäß angezeigt. Weitere Informationen finden Sie unter [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





