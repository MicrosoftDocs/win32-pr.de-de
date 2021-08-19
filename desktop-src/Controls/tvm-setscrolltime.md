---
title: TVM_SETSCROLLTIME (Commctrl.h)
description: Legt die maximale Bildlaufzeit für das Strukturansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetScrollTime-Makros senden.
ms.assetid: b0ad81ba-0621-42b7-8fe1-f3bd5bc16d6a
keywords:
- TVM_SETSCROLLTIME meldungssteuerelemente Windows
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
ms.openlocfilehash: 4c9ca3392de81a712aa6be7dc2addb87eedf65af4aa77958e5b7f5fbb2eafc87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408487"
---
# <a name="tvm_setscrolltime-message"></a>TVM \_ SETSCROLLTIME-Meldung

Legt die maximale Bildlaufzeit für das Strukturansicht-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetScrollTime-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Neue maximale Bildlaufzeit in Millisekunden.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige maximale Bildlaufzeit in Millisekunden zurück.

## <a name="remarks"></a>Hinweise

Die maximale Scrollzeit ist die längste Zeit, die ein Bildlaufvorgang dauern kann. Das Scrollen wird so angepasst, dass der Bildlauf innerhalb der maximalen Scrollzeit erfolgt. Ein Bildlaufvorgang kann weniger Zeit als das Maximum dauern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TVM \_ GETSCROLLTIME**](tvm-getscrolltime.md)
</dt> </dl>

 

 





