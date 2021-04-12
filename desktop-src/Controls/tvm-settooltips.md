---
title: TVM_SETTOOLTIPS Meldung (kommstrg. h)
description: Legt das untergeordnete ToolTip-Steuerelement eines Strukturansicht-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des TreeView- \_ Makros SetToolTips senden.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- Windows-Steuerelemente für TVM_SETTOOLTIPS Meldung
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
ms.openlocfilehash: efd9d5957a38d873993405a5283545472433e958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103623"
---
# <a name="tvm_settooltips-message"></a>TVM- \_ SetToolTips-Meldung

Legt das untergeordnete ToolTip-Steuerelement eines Strukturansicht-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Makros \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für ein QuickInfo-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das QuickInfo-Steuerelement zurück, das zuvor für das Strukturansicht-Steuerelement festgelegt wurde, oder **null** , wenn keine Quick Infos verwendet wurden

## <a name="remarks"></a>Bemerkungen

Beim Erstellen wird von Strukturansicht-Steuerelementen automatisch ein untergeordnetes QuickInfo-Steuerelement erstellt. Um zu verhindern, dass ein Strukturansicht-Steuerelement Quick Infos verwendet, erstellen Sie das Steuerelement mit dem [**\_ witooltips**](tree-view-control-window-styles.md) -Stil "TVs".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ gettooltips**](tvm-gettooltips.md)
</dt> </dl>

 

 





