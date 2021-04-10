---
title: TVM_GETTEXTCOLOR Meldung (kommstrg. h)
description: Ruft die aktuelle Textfarbe des-Steuer Elements ab. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ gettextcolor-Makros senden.
ms.assetid: fe1aa2e8-fdf2-48d1-936b-6d6bc8e589f4
keywords:
- Windows-Steuerelemente für TVM_GETTEXTCOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899fc68847fea937a6f62bff6367eeac5570a5a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040351"
---
# <a name="tvm_gettextcolor-message"></a>TVM \_ gettextcolor-Meldung

Ruft die aktuelle Textfarbe des-Steuer Elements ab. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ gettextcolor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die aktuelle Textfarbe darstellt. Wenn dieser Wert-1 ist, verwendet das Steuerelement die System Farbe für die Textfarbe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ SetTextColor**](tvm-settextcolor.md)
</dt> </dl>

 

