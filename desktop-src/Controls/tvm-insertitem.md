---
title: TVM_INSERTITEM Meldung (kommstrg. h)
description: Fügt ein neues Element in ein Strukturansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ InsertItem-Makros senden.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- Windows-Steuerelemente für TVM_INSERTITEM Meldung
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 719de4c2391ff924c9f6deb8cb4206cfdb56c3ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858752"
---
# <a name="tvm_insertitem-message"></a>TVM \_ InsertItem-Meldung

Fügt ein neues Element in ein Strukturansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) -Struktur, die die Attribute des Struktur Ansichts Elements angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das **HTREEITEM** -Handle für das neue Element zurück, wenn erfolgreich, andernfalls **null** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVM \_ Insertitemw** (Unicode) und **TVM \_ insertitema** (ANSI)<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TVN \_ endlabeledit](tvn-endlabeledit.md)
</dt> </dl>

 

 





