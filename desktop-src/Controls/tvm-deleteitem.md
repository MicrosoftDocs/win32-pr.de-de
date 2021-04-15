---
title: TVM_DELETEITEM Meldung (kommstrg. h)
description: Entfernt ein Element und alle untergeordneten Elemente aus einem Strukturansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ DeleteItem-Makros senden.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- Windows-Steuerelemente für TVM_DELETEITEM Meldung
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
ms.openlocfilehash: 8783fd5acdf7319699cdc67cbb3ea075e4dbbc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476953"
---
# <a name="tvm_deleteitem-message"></a>TVM \_ DeleteItem-Meldung

Entfernt ein Element und alle untergeordneten Elemente aus einem Strukturansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

**HTREEITEM** -Handle für das Element, das gelöscht werden soll. Wenn *LPARAM* auf TVI \_ root oder auf **null** festgelegt ist, werden alle Elemente gelöscht. Sie können auch das [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) -Makro verwenden, um alle Elemente zu löschen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Es ist nicht sicher, Elemente als Reaktion auf eine Benachrichtigung zu löschen, wie z. [b. TVN \_ selchanging](tvn-selchanging.md).

Wenn ein Element gelöscht wird, ist das zugehörige Handle ungültig und kann nicht verwendet werden.

Das übergeordnete Fenster empfängt einen [TVN \_ DeleteItem](tvn-deleteitem.md) -Benachrichtigungs Code, wenn jedes Element entfernt wird.

Wenn die Element Bezeichnung bearbeitet wird, wird der Bearbeitungsvorgang abgebrochen, und das übergeordnete Fenster empfängt den [TVN \_ endlabeledit](tvn-endlabeledit.md) -Benachrichtigungs Code.

Wenn Sie alle Elemente in einem Strukturansicht-Steuerelement mit dem " [**TVs"- \_ NoScroll**](tree-view-control-window-styles.md) -Stil löschen, werden die Elemente, die später hinzugefügt werden, möglicherweise nicht Weitere Informationen finden Sie unter [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





