---
title: DTM_CLOSEMONTHCAL (Commctrl.h)
description: Schließt ein DTP-Steuerelement (Date and Time Picker). Senden Sie diese Nachricht explizit oder mithilfe des DateTime \_ CloseMonthCal-Makros.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- DTM_CLOSEMONTHCAL meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f458592d2842625b9826eda5963c66cbd182e3f052a2b2a70ff5219a054e8cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878240"
---
# <a name="dtm_closemonthcal-message"></a>MESSAGE \_ CLOSEMONTHCAL -Meldung von CLOSEMONTHCAL

Schließt ein DTP-Steuerelement (Date and Time Picker). Senden Sie diese Nachricht explizit oder mithilfe des [**DateTime \_ CloseMonthCal-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Zerstört das Steuerelement und sendet eine [DTN \_ CLOSEUP-Benachrichtigung,](dtn-closeup.md) dass das Steuerelement geschlossen wird, anstatt dass das Steuerelement geöffnet wird (dropdown-down wie in der [DTN-DROPDOWNbenachrichtigung), \_ ](dtn-dropdown.md) an das übergeordnete Element des Steuerelements.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[\_DTN-DROPDOWNliste](dtn-dropdown.md)
</dt> <dt>

[DTN \_ CLOSEUP](dtn-closeup.md)
</dt> </dl>

 

 





