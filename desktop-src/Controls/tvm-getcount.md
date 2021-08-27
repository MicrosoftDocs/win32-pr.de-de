---
title: TVM_GETCOUNT (Commctrl.h)
description: Ruft die Anzahl der Elemente in einem Strukturansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetCount-Makros senden.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- TVM_GETCOUNT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fce2d3ed6580acc875007ff3962bbeb21e9c0d3c3cb38128a2339da79597f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060350"
---
# <a name="tvm_getcount-message"></a>TVM \_ GETCOUNT-Nachricht

Ruft die Anzahl der Elemente in einem Strukturansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetCount-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Elemente zurück.

## <a name="remarks"></a>Hinweise

Die von [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) zurückgegebene Knotenanzahl ist auf ganzzahlige Werte beschränkt. Wenn Sie einen Knoten über 32767 hinaus hinzufügen, gibt das Makro einen negativen Wert zurück. Nach dem Hinzufügen von 65536 Knoten wird die Anzahl auf 0 (null) zurückgesetzt. In diesem Fall wird das Strukturansicht-Steuerelement ohne Scrollleisten leer angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





