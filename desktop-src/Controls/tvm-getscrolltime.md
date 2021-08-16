---
title: TVM_GETSCROLLTIME (Commctrl.h)
description: Ruft die maximale Bildlaufzeit für das Strukturansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetScrollTime-Makros senden.
ms.assetid: 992d1906-cda3-4ac7-ba90-c681c551ac2e
keywords:
- TVM_GETSCROLLTIME von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TVM_GETSCROLLTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e026a463476d5625f7632d7b6679ce94ca2c8ab6d8c6a050d8938bd46d9858b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408497"
---
# <a name="tvm_getscrolltime-message"></a>TVM \_ GETSCROLLTIME-Meldung

Ruft die maximale Bildlaufzeit für das Strukturansicht-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetScrollTime-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die maximale Bildlaufzeit in Millisekunden zurück.

## <a name="remarks"></a>Hinweise

Die maximale Scrollzeit ist die längste Zeit, die ein Bildlaufvorgang dauern kann. Der Bildlauf wird so angepasst, dass der Bildlauf innerhalb der maximalen Scrollzeit erfolgt. Ein Bildlaufvorgang kann weniger Zeit als das Maximum dauern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TVM \_ SETSCROLLTIME**](tvm-setscrolltime.md)
</dt> </dl>

 

 





