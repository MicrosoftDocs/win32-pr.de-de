---
title: TVM_SHOWINFOTIP (Commctrl.h)
description: Zeigt die Infotip für ein angegebenes Element in einem Strukturansicht-Steuerelement an. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ ShowInfoTip-Makros senden.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- TVM_SHOWINFOTIP von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1cf61511e8c9e69c42d89f99fc4ddae90de78701e5e75170ff1b793671120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913920"
---
# <a name="tvm_showinfotip-message"></a>TVM \_ SHOWINFOTIP-Nachricht

Zeigt die Infotip für ein angegebenes Element in einem Strukturansicht-Steuerelement an. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ ShowInfoTip-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Handle für das Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Die meisten Anwendungen verwenden diese Meldung nicht. Infotips werden automatisch angezeigt. Weitere Informationen finden Sie unter Using Tree-view Infotips (Verwenden von Infotips für Strukturansichten) in der Übersicht über [Tree-View Steuerelemente.](tree-view-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





