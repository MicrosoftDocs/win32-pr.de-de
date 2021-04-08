---
title: TVM_GETVISIBLECOUNT Meldung (kommstrg. h)
description: Ruft die Anzahl der Elemente ab, die im Client Fenster eines Strukturansicht-Steuer Elements vollständig sichtbar sein können. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetVisibleCount-Makros senden.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- Windows-Steuerelemente für TVM_GETVISIBLECOUNT Meldung
topic_type:
- apiref
api_name:
- TVM_GETVISIBLECOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1927d21741b109c5f00aa964b058dc0c34732529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949589"
---
# <a name="tvm_getvisiblecount-message"></a>TVM \_ GetVisibleCount-Meldung

Ruft die Anzahl der Elemente ab, die im Client Fenster eines Strukturansicht-Steuer Elements vollständig sichtbar sein können. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetVisibleCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Elemente zurück, die im Client Fenster des Strukturansicht-Steuer Elements vollständig sichtbar sein können.

## <a name="remarks"></a>Bemerkungen

Die Anzahl der Elemente, die vollständig sichtbar sein können, ist möglicherweise größer als die Anzahl der Elemente im Steuerelement. Das-Steuerelement berechnet diesen Wert durch Aufteilen der Höhe des Client Fensters durch die Höhe eines Elements.

Beachten Sie, dass der Rückgabewert die Anzahl der Elemente ist, die *vollständig* sichtbar sein können. Wenn Sie alle 20 Elemente und einen Teil von einem weiteren Element sehen können, ist der Rückgabewert 20.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





