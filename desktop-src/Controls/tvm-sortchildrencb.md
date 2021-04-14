---
title: TVM_SORTCHILDRENCB Meldung (kommstrg. h)
description: Sortiert Struktur Ansichts Elemente mithilfe einer Anwendungs definierten Rückruffunktion, die die Elemente vergleicht. Sie können diese Nachricht explizit oder mit dem TreeView- \_ Makro "SortChildren-CB" senden.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- Windows-Steuerelemente für TVM_SORTCHILDRENCB Meldung
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
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478945"
---
# <a name="tvm_sortchildrencb-message"></a>TVM \_ SortChildren-Nachricht

Sortiert Struktur Ansichts Elemente mithilfe einer Anwendungs definierten Rückruffunktion, die die Elemente vergleicht. Sie können diese Nachricht explizit oder mit dem [**TreeView-Makro " \_ SortChildren-CB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Reserviert. Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**tvsortcb**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) -Struktur. Der **lpfncompare** -Member ist die Adresse der Anwendungs definierten Rückruffunktion, die während des Sortier Vorgangs aufgerufen wird, wenn die relative Reihenfolge zweier Listenelemente verglichen werden muss. Weitere Informationen zur Rückruffunktion finden Sie in der Beschreibung von **tvsortcb**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





