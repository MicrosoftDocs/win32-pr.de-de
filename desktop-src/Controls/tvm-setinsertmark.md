---
title: TVM_SETINSERTMARK-Nachricht (Commctrl.h)
description: Legt die Einfügemarke in einem Strukturansichtssteuerelement fest. Sie können diese Nachricht explizit oder mit dem TreeView \_ SetInsertMark-Makro senden.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- TVM_SETINSERTMARK Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 0c3004395dcc7ea0b83af2fc2b7dae370c303228f79599215d5b6d264379b793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875630"
---
# <a name="tvm_setinsertmark-message"></a>TVM \_ SETINSERTMARK-Nachricht

Legt die Einfügemarke in einem Strukturansichtssteuerelement fest. Sie können diese Nachricht explizit oder mit dem [**TreeView \_ SetInsertMark-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**BOOL-Wert,** der angibt, ob die Einfügemarke vor oder nach dem angegebenen Element platziert wird. Wenn dieses Argument ungleich 0 (null) ist, wird die Einfügemarke hinter dem Element platziert. Wenn dieses Argument 0 (null) ist, wird die Einfügemarke vor dem Element platziert.

</dd> <dt>

*lParam* 
</dt> <dd>

**HTREEITEM,** das angibt, an welchem Element die Einfügemarke platziert wird. Wenn dieses Argument **NULL** ist, wird die Einfügemarke entfernt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben.

## <a name="remarks"></a>Hinweise

In einigen Fällen kann das Einfügezeichen an zwei Stellen angezeigt werden, nachdem ein Knoten erweitert wurde. Wenn Sie Einfügezeichen verwenden, wird empfohlen, nach dem Erweitern eines Knotens eine Aktualisierung des Steuerelements zu erzwingen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





