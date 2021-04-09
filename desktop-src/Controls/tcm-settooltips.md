---
title: TCM_SETTOOLTIPS Meldung (kommstrg. h)
description: Weist einem Registerkarten-Steuerelement ein ToolTip-Steuerelement zu. Sie können diese Nachricht explizit oder mithilfe des tabctrl- \_ Makros SetToolTips senden.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- Windows-Steuerelemente für TCM_SETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739872"
---
# <a name="tcm_settooltips-message"></a>TCM- \_ SetToolTips-Meldung

Weist einem Registerkarten-Steuerelement ein ToolTip-Steuerelement zu. Sie können diese Nachricht explizit oder mithilfe des [**tabctrl-Makros \_ SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das QuickInfo-Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Sie können das QuickInfo-Steuerelement, das einem Registerkarten-Steuerelement zugeordnet ist, mithilfe der [**TCM \_ gettooltips**](tcm-gettooltips.md) -Nachricht abrufen

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





