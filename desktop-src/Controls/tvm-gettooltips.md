---
title: TVM_GETTOOLTIPS Meldung (kommstrg. h)
description: Ruft das Handle für das untergeordnete ToolTip-Steuerelement ab, das von einem Strukturansicht-Steuerelement verwendet wird. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ gettooltips-Makros senden.
ms.assetid: 65e8189e-ae3e-4268-b1ed-bb0d88f2cbe3
keywords:
- Windows-Steuerelemente für TVM_GETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305aaa05df5b72ffde709e4cf3b3e06d47c43448
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475897"
---
# <a name="tvm_gettooltips-message"></a>TVM \_ gettooltips-Meldung

Ruft das Handle für das untergeordnete ToolTip-Steuerelement ab, das von einem Strukturansicht-Steuerelement verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ gettooltips**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das untergeordnete QuickInfo-Steuerelement zurück, oder **null** , wenn das Steuerelement keine Quick Infos verwendet.

## <a name="remarks"></a>Bemerkungen

Beim Erstellen wird von Strukturansicht-Steuerelementen automatisch ein untergeordnetes QuickInfo-Steuerelement erstellt. Damit ein Strukturansicht-Steuerelement keine Quick Infos verwendet, erstellen Sie das Steuerelement mit [**dem \_ witooltips**](tree-view-control-window-styles.md) -Stil "TVs".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM- \_ SetToolTips**](tvm-settooltips.md)
</dt> </dl>

 

 





