---
title: TVM_SETTOOLTIPS (Commctrl.h)
description: Legt das untergeordnete QuickInfo-Steuerelement eines Strukturansicht-Steuerelements fest. Sie können diese Nachricht explizit oder mithilfe des \_ TreeView-Makros SetToolTips senden.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- TVM_SETTOOLTIPS von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd18a5217db0d105841722d208904c1b65199504750576acf1ff8035f31bd585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913960"
---
# <a name="tvm_settooltips-message"></a>TVM \_ SETTOOLTIPS-Meldung

Legt das untergeordnete QuickInfo-Steuerelement eines Strukturansicht-Steuerelements fest. Sie können diese Nachricht explizit oder mithilfe des [**\_ TreeView-Makros SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für ein QuickInfo-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das QuickInfo-Steuerelement zurück, das zuvor für das Strukturansicht-Steuerelement festgelegt wurde, oder **NULL,** wenn QuickInfos zuvor nicht verwendet wurden.

## <a name="remarks"></a>Hinweise

Nach der Erstellung erstellen Strukturansichtssteuerelemente automatisch ein untergeordnetes QuickInfo-Steuerelement. Um zu verhindern, dass ein Strukturansicht-Steuerelement QuickInfos verwendet, erstellen Sie das Steuerelement mit dem [**TVS \_ NOTOOLTIPS-Stil.**](tree-view-control-window-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ GETTOOLTIPS**](tvm-gettooltips.md)
</dt> </dl>

 

 





