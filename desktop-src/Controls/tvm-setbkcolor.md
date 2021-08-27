---
title: TVM_SETBKCOLOR Nachricht (Commctrl.h)
description: Legt die Hintergrundfarbe des Steuerelements fest. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetBkColor-Makros senden.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- TVM_SETBKCOLOR Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0609a15be2b8e05b1f8ca8f4f999cd4888ee946969c25f5bc1d86420b7529f2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060120"
---
# <a name="tvm_setbkcolor-message"></a>TVM \_ SETBKCOLOR-Nachricht

Legt die Hintergrundfarbe des Steuerelements fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetBkColor-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF-Wert,**](/windows/desktop/gdi/colorref) der die neue Hintergrundfarbe enthält. Wenn dieser Wert -1 ist, wird das Steuerelement auf die Systemfarbe für die Hintergrundfarbe zurückgesetzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF-Wert**](/windows/desktop/gdi/colorref) zurück, der die vorherige Hintergrundfarbe darstellt. Wenn dieser Wert -1 ist, verwendet das Steuerelement die Systemfarbe für die Hintergrundfarbe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ GETBKCOLOR**](tvm-getbkcolor.md)
</dt> </dl>

 

