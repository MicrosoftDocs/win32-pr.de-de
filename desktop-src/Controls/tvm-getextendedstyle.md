---
title: TVM_GETEXTENDEDSTYLE (Commctrl.h)
description: Ruft den erweiterten Stil für ein Strukturansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des TreeView \_ GetExtendedStyle-Makros.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- TVM_GETEXTENDEDSTYLE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93eb22b3dfdbe05365d28a7c93bfa9df3619796f9b4ae9ec603c74da252c5a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834200"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a>TVM_GETEXTENDEDSTYLE (Commctrl.h)

Ruft den erweiterten Stil für ein Strukturansicht-Steuerelement ab. Senden Sie diese Nachricht explizit oder mithilfe des [**TreeView \_ GetExtendedStyle-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert des erweiterten Stils zurück. Weitere Informationen zu Stilen finden Sie unter [Strukturansicht-Steuerelement Erweiterte Stile.](tree-view-control-window-extended-styles.md)

## <a name="remarks"></a>Hinweise

Die erweiterten Stile für ein Strukturansicht-Steuerelement haben nichts mit den erweiterten Stilen zu tun, die mit der [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) oder der [**Funktion SetWindowLong verwendet werden.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

