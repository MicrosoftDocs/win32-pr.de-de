---
title: MCM_SETCALID Meldung (kommstrg. h)
description: Legt die Kalender-ID für das angegebene Kalender Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des "monthcal \_ setcalid"-Makros senden.
ms.assetid: 4b9d06f5-0784-4a17-b401-982206d4be67
keywords:
- Windows-Steuerelemente für MCM_SETCALID Meldung
topic_type:
- apiref
api_name:
- MCM_SETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a661a685062fe737a1927c3a6ab455e8499c6ca9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040241"
---
# <a name="mcm_setcalid-message"></a>MCM \_ -setcalid-Meldung

Legt die Kalender-ID für das angegebene Kalender Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des " [**monthcal \_ setcalid"-**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalid) Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Kalender-ID. Eine der-Konstanten des [Kalender Bezeichner](/windows/desktop/Intl/calendar-identifiers) .

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

