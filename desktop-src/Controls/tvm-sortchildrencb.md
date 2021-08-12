---
title: TVM_SORTCHILDRENCB-Nachricht (Commctrl.h)
description: Sortiert Strukturansichtselemente mithilfe einer anwendungsdefiniert Rückruffunktion, die die Elemente vergleicht. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SortChildrenCB-Makros senden.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- TVM_SORTCHILDRENCB Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45f0ec311cc5ce0f972f3363ea97cd42874ca85807bf852296de0283fccc95c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669476"
---
# <a name="tvm_sortchildrencb-message"></a>TVM \_ SORTCHILDRENCB-Nachricht

Sortiert Strukturansichtselemente mithilfe einer anwendungsdefiniert Rückruffunktion, die die Elemente vergleicht. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SortChildrenCB-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TVSORTCB-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) Der **lpfnCompare-Member** ist die Adresse der anwendungsdefinierte Rückruffunktion, die während des Sortiervorgangs jedes Mal aufgerufen wird, wenn die relative Reihenfolge von zwei Listenelementen verglichen werden muss. Weitere Informationen zur Rückruffunktion finden Sie in der Beschreibung von **TVSORTCB**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





