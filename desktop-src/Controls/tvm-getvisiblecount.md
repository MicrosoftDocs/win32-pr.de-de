---
title: TVM_GETVISIBLECOUNT Meldung (Commctrl.h)
description: Ruft die Anzahl der Elemente ab, die im Clientfenster eines Strukturansichtssteuerelements vollständig sichtbar sein können. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetVisibleCount-Makros senden.
ms.assetid: c3519543-3fb2-4ecf-ac01-905d0946cb1b
keywords:
- TVM_GETVISIBLECOUNT Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 07604eed3d3ece140d33bb9c612a2f898f6de02785f2c9916332de60358693fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698660"
---
# <a name="tvm_getvisiblecount-message"></a>TVM \_ GETVISIBLECOUNT-Nachricht

Ruft die Anzahl der Elemente ab, die im Clientfenster eines Strukturansichtssteuerelements vollständig sichtbar sein können. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetVisibleCount-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der Elemente zurück, die im Clientfenster des Strukturansichtssteuerelements vollständig sichtbar sein können.

## <a name="remarks"></a>Hinweise

Die Anzahl der Elemente, die vollständig sichtbar sein können, kann größer als die Anzahl der Elemente im Steuerelement sein. Das -Steuerelement berechnet diesen Wert, indem die Höhe des Clientfensters durch die Höhe eines Elements dividiert wird.

Beachten Sie, dass der Rückgabewert die Anzahl der Elemente ist, die *vollständig* sichtbar sein können. Wenn Sie alle 20 Elemente und einen Teil eines weiteren Elements sehen können, ist der Rückgabewert 20.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





