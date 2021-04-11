---
title: TCM_DESELECTALL Meldung (kommstrg. h)
description: Setzt Elemente in einem Registerkarten-Steuerelement zurück und löscht alle, die auf den tcis- \_ ButtonPressed-Zustand festgelegt wurden. Sie können diese Nachricht explizit oder mithilfe des tabctrl- \_ Makros DeselectAll senden.
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- Windows-Steuerelemente für TCM_DESELECTALL Meldung
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105747"
---
# <a name="tcm_deselectall-message"></a>TCM- \_ DeselectAll-Nachricht

Setzt Elemente in einem Registerkarten-Steuerelement zurück und löscht alle, die auf den [**tcis- \_ ButtonPressed**](tab-control-item-states.md) -Zustand festgelegt wurden. Sie können diese Nachricht explizit oder mithilfe des [**tabctrl-Makros \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag, das den Gültigkeitsbereich der Elementauswahl angibt. Wenn dieser Parameter auf **false** festgelegt ist, werden alle Registerkarten Elemente zurückgesetzt. Wenn der Wert auf **true** festgelegt ist, werden alle Registerkarten Elemente mit Ausnahme der aktuell ausgewählten Elemente zurückgesetzt.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Diese Meldung ist nur dann sinnvoll, wenn das Style-Flag der [**TCS- \_ Schalt**](tab-control-styles.md) Flächen festgelegt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





