---
title: TVM_SETSCROLLTIME Meldung (kommstrg. h)
description: Legt die maximale Scrollzeit für das Strukturansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ setscrolltime-Makros senden.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- Windows-Steuerelemente für TVM_SETSCROLLTIME Meldung
topic_type:
- apiref
api_name:
- TVM_SETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fab2f662b5ec641d9ffc6cc276f2196d2613e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338765"
---
# <a name="tvm_setscrolltime-message"></a>TVM- \_ setscrolltime-Meldung

Legt die maximale Scrollzeit für das Strukturansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView- \_ setscrolltime**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Neue maximale Scrollzeit in Millisekunden.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige maximale Scrollzeit in Millisekunden zurück.

## <a name="remarks"></a>Bemerkungen

Die maximale Scrollzeit ist die längste Zeitspanne, die ein scrollvorgang ausführen kann. Der Bildlauf wird so angepasst, dass der Bildlauf innerhalb der maximalen Scrollzeit stattfindet. Ein scrollvorgang kann weniger Zeit in Anspruch nehmen als das Maximum.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ getscrolltime**](tvm-getscrolltime.md)
</dt> </dl>

 

 





