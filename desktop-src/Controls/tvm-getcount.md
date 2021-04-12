---
title: TVM_GETCOUNT Meldung (kommstrg. h)
description: Ruft die Anzahl der Elemente in einem Strukturansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetCount-Makros senden.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- Windows-Steuerelemente für TVM_GETCOUNT Meldung
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
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478480"
---
# <a name="tvm_getcount-message"></a>TVM \_ GetCount-Meldung

Ruft die Anzahl der Elemente in einem Strukturansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Elemente zurück.

## <a name="remarks"></a>Bemerkungen

Die von [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) zurückgegebene Knoten Anzahl ist auf ganzzahlige Werte beschränkt. Wenn Sie einen Knoten außer 32767 hinzufügen, gibt das Makro einen negativen Wert zurück. Nach dem Hinzufügen von 65536 Knoten wird die Anzahl auf 0 zurückgesetzt. Wenn dies auftritt, wird das Strukturansicht-Steuerelement ohne Scrollleisten leer angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





