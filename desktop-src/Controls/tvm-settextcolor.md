---
title: TVM_SETTEXTCOLOR Meldung (kommstrg. h)
description: Legt die Textfarbe des-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetTextColor-Makros senden.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- Windows-Steuerelemente für TVM_SETTEXTCOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742000"
---
# <a name="tvm_settextcolor-message"></a>TVM- \_ SetTextColor-Meldung

Legt die Textfarbe des-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue Textfarbe enthält. Wenn dieses Argument-1 ist, verwendet das Steuerelement die System Farbe für die Textfarbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **COLORREF** -Wert zurück, der die vorherige Textfarbe darstellt. Wenn dieser Wert-1 ist, verwendet das Steuerelement die System Farbe für die Textfarbe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ gettextcolor**](tvm-gettextcolor.md)
</dt> </dl>

 

