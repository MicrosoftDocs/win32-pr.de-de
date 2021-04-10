---
title: DTM_CLOSEMONTHCAL Meldung (kommstrg. h)
description: Schließt ein DTP-Steuerelement (Datums-und Zeitauswahl). Senden Sie diese Nachricht explizit oder mithilfe des "DateTime \_ closemonthcal"-Makros.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- Windows-Steuerelemente für DTM_CLOSEMONTHCAL Meldung
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
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040186"
---
# <a name="dtm_closemonthcal-message"></a>DTM \_ closemonthcal-Nachricht

Schließt ein DTP-Steuerelement (Datums-und Zeitauswahl). Senden Sie diese Nachricht explizit oder mithilfe des " [**DateTime \_ closemonthcal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) "-Makros.

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

## <a name="remarks"></a>Bemerkungen

Zerstört das-Steuerelement und sendet eine [Dtn- \_ closeup](dtn-closeup.md) -Benachrichtigung, dass das-Steuerelement geschlossen wird, anstatt das-Steuerelement zu öffnen (in der [Dtn- \_ Dropdown](dtn-dropdown.md) Benachrichtigung), an das übergeordnete Steuerelement des Steuer Elements.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[DTN- \_ Dropdown](dtn-dropdown.md)
</dt> <dt>

[DTN- \_ Schließung](dtn-closeup.md)
</dt> </dl>

 

 





