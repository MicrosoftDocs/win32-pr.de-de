---
title: TCM_SETTOOLTIPS Nachricht (Commctrl.h)
description: Weist einem Registerkartensteuerelement ein QuickInfo-Steuerelement zu. Sie können diese Nachricht explizit oder mithilfe des \_ TabCtrl-Makros SetToolTips senden.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- TCM_SETTOOLTIPS Windows-Steuerelementen
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
ms.openlocfilehash: c8bfec3b7272ceae3dcbf1781e3bb17a988f2252b3c0a74822677bff6ea39209
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104690"
---
# <a name="tcm_settooltips-message"></a>TCM \_ SETTOOLTIPS-Nachricht

Weist einem Registerkartensteuerelement ein QuickInfo-Steuerelement zu. Sie können diese Nachricht explizit oder mithilfe des [**\_ TabCtrl-Makros SetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) senden.

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

## <a name="remarks"></a>Hinweise

Sie können das QuickInfo-Steuerelement abrufen, das einem Registerkartensteuerelement zugeordnet ist, indem Sie die [**TCM \_ GETTOOLTIPS-Nachricht**](tcm-gettooltips.md) verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





