---
title: TVM_SETINSERTMARK Meldung (kommstrg. h)
description: Legt die Einfügemarke in einem Strukturansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ mapresertmark-Makros senden.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- Windows-Steuerelemente für TVM_SETINSERTMARK Meldung
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5a9cc9b05e9cd7dc3281d778734bee1048ffd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858998"
---
# <a name="tvm_setinsertmark-message"></a>TVM- \_ Nachricht "tmark"

Legt die Einfügemarke in einem Strukturansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView- \_ mapresertmark**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**Boolescher** Wert, der angibt, ob die Einfügemarke vor oder nach dem angegebenen Element eingefügt wird. Wenn dieses Argument ungleich 0 (null) ist, wird die Einfügemarke hinter dem Element platziert. Wenn dieses Argument 0 (null) ist, wird die Einfügemarke vor dem Element platziert.

</dd> <dt>

*lParam* 
</dt> <dd>

**HTREEITEM** , das angibt, an welchem Punkt die Einfügemarke platziert werden soll. Wenn dieses Argument **null** ist, wird die Einfügemarke entfernt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

In einigen Fällen kann die Einfügemarke an zwei Stellen angezeigt werden, nachdem ein Knoten erweitert wurde. Wenn Sie Einfügezeichen verwenden, wird empfohlen, nach dem Erweitern eines Knotens eine Aktualisierung des Steuer Elements zu erzwingen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





