---
title: TCM_GETTOOLTIPS Meldung (kommstrg. h)
description: Ruft das Handle für das QuickInfo-Steuerelement ab, das einem Register Steuerelement zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ gettooltips-Makros senden.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- Windows-Steuerelemente für TCM_GETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e49334a1fa7124dd6e7a0f0b739cd1ebd24b51b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105735"
---
# <a name="tcm_gettooltips-message"></a>TCM \_ gettooltips-Meldung

Ruft das Handle für das QuickInfo-Steuerelement ab, das einem Register Steuerelement zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ gettooltips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das QuickInfo-Steuerelement zurück, wenn erfolgreich, andernfalls **null** .

## <a name="remarks"></a>Bemerkungen

Ein Registerkarten-Steuerelement erstellt ein QuickInfo-Steuerelement, wenn es den [**TCS- \_ Tooltips**](tab-control-styles.md) -Stil Sie können einem Registerkarten-Steuerelement auch ein QuickInfo-Steuerelement mithilfe der [**TCM- \_ SetToolTips**](tcm-settooltips.md) -Nachricht zuweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





