---
title: TVM_SETTEXTCOLOR (Commctrl.h)
description: Legt die Textfarbe des Steuerelements fest. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetTextColor-Makros senden.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- TVM_SETTEXTCOLOR von Windows-Steuerelementen
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
ms.openlocfilehash: 41559abd6724ee9c8ce9f86cfcff092ad13d949a80a55d45ff996f36b284932d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503610"
---
# <a name="tvm_settextcolor-message"></a>TVM \_ SETTEXTCOLOR-Meldung

Legt die Textfarbe des Steuerelements fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetTextColor-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

[**COLORREF-Wert,**](/windows/desktop/gdi/colorref) der die neue Textfarbe enthält. Wenn dieses Argument -1 ist, verwendet das Steuerelement wieder die Systemfarbe für die Textfarbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **COLORREF-Wert** zurück, der die vorherige Textfarbe darstellt. Wenn dieser Wert -1 ist, hat das Steuerelement die Systemfarbe für die Textfarbe verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md)
</dt> </dl>

 

