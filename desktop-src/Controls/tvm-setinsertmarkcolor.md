---
title: TVM_SETINSERTMARKCOLOR Meldung (kommstrg. h)
description: Legt die Farbe fest, die zum Zeichnen der Einfügemarke für die Strukturansicht verwendet wird. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ mapresertmarkcolor-Makros senden.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- Windows-Steuerelemente für TVM_SETINSERTMARKCOLOR Meldung
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92668b1137b089f9a09cc9a34d63d472742bce4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104175"
---
# <a name="tvm_setinsertmarkcolor-message"></a>TVM-Meldung "". \_

Legt die Farbe fest, die zum Zeichnen der Einfügemarke für die Strukturansicht verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**TreeView- \_ mapresertmarkcolor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue einfügemarkierungs Farbe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **COLORREF** -Wert zurück, der die vorherige Einfügemarke enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ getinsertmarkcolor**](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

