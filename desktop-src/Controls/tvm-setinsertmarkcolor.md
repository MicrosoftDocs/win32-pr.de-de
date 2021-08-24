---
title: TVM_SETINSERTMARKCOLOR (Commctrl.h)
description: Legt die Farbe fest, die zum Zeichnen der Einfügemarke für die Strukturansicht verwendet wird. Sie können diese Nachricht explizit oder mithilfe des \_ TreeView-Makros SetInsertMarkColor senden.
ms.assetid: c82304a8-3726-42c0-81e7-90d8f8205ead
keywords:
- TVM_SETINSERTMARKCOLOR meldungssteuerelemente Windows
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
ms.openlocfilehash: 05d5fd9984b77c99a13e1c7eab24c231e0ce7f601ecb79f8747cdf7ea3011327
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636760"
---
# <a name="tvm_setinsertmarkcolor-message"></a>TVM \_ SETINSERTMARKCOLOR-Meldung

Legt die Farbe fest, die zum Zeichnen der Einfügemarke für die Strukturansicht verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**\_ TreeView-Makros SetInsertMarkColor**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF-Wert,**](/windows/desktop/gdi/colorref) der die neue Einfügemarke enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **COLORREF-Wert** zurück, der die vorherige Einfügemarke enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ GETINSERTMARKCOLOR**](tvm-getinsertmarkcolor.md)
</dt> </dl>

 

