---
title: TVM_INSERTITEM (Commctrl.h)
description: Fügt ein neues Element in ein Strukturansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ InsertItem-Makros senden.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- TVM_INSERTITEM meldungssteuerelemente Windows
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
ms.openlocfilehash: 85f8a324613820b94e0bd2c49d8fa78136038471f820dd2b9ed8e38ace15f0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060190"
---
# <a name="tvm_insertitem-message"></a>TVM \_ INSERTITEM-Meldung

Fügt ein neues Element in ein Strukturansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ InsertItem-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TVINSERTSTRUCT-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) die die Attribute des Strukturansichtselements angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das **HTREEITEM-Handle** an das neue Element zurück, falls erfolgreich, **andernfalls NULL.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVM \_ INSERTITEMW** (Unicode) und **TVM \_ INSERTITEMA** (ANSI)<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TVN \_ ENDLABELEDIT](tvn-endlabeledit.md)
</dt> </dl>

 

 





