---
title: TVM_SETBKCOLOR Meldung (kommstrg. h)
description: Legt die Hintergrundfarbe des-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetBkColor-Makros senden.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- Windows-Steuerelemente für TVM_SETBKCOLOR Meldung
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
ms.openlocfilehash: 151aef7aa61e7c66d436d0c90f2481fada017059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858999"
---
# <a name="tvm_setbkcolor-message"></a>TVM- \_ SetBkColor-Meldung

Legt die Hintergrundfarbe des-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue Hintergrundfarbe enthält. Wenn dieser Wert-1 ist, wird das Steuerelement wieder auf die System Farbe für die Hintergrundfarbe zurückgesetzt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die vorherige Hintergrundfarbe darstellt. Wenn dieser Wert-1 ist, verwendet das Steuerelement die System Farbe für die Hintergrundfarbe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ GetBkColor**](tvm-getbkcolor.md)
</dt> </dl>

 

