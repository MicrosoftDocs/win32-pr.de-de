---
title: TVM_GETBKCOLOR Meldung (kommstrg. h)
description: Ruft die aktuelle Hintergrundfarbe des-Steuer Elements ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetBkColor-Makros senden.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- Windows-Steuerelemente für TVM_GETBKCOLOR Meldung
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
ms.openlocfilehash: 8077bc9655c088aceefe239ed019cc45874d38ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345324"
---
# <a name="tvm_getbkcolor-message"></a>TVM \_ GetBkColor-Meldung

Ruft die aktuelle Hintergrundfarbe des-Steuer Elements ab. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die aktuelle Hintergrundfarbe darstellt. Wenn dieser Wert-1 ist, verwendet das Steuerelement die System Farbe für die Hintergrundfarbe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ SetBkColor**](tvm-setbkcolor.md)
</dt> </dl>

 

