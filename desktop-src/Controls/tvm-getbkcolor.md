---
title: TVM_GETBKCOLOR (Commctrl.h)
description: Ruft die aktuelle Hintergrundfarbe des Steuerelements ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetBkColor-Makros senden.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- TVM_GETBKCOLOR von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a5a6530b1aada1fab06c0b353d7ead666e61f0f796b890d1f5c56fe0be094b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088450"
---
# <a name="tvm_getbkcolor-message"></a>TVM \_ GETBKCOLOR-Nachricht

Ruft die aktuelle Hintergrundfarbe des Steuerelements ab. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetBkColor-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF-Wert**](/windows/desktop/gdi/colorref) zurück, der die aktuelle Hintergrundfarbe darstellt. Wenn dieser Wert -1 ist, verwendet das Steuerelement die Systemfarbe für die Hintergrundfarbe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ SETBKCOLOR**](tvm-setbkcolor.md)
</dt> </dl>

 

