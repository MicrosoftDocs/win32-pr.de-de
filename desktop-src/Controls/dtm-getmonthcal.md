---
title: DTM_GETMONTHCAL Meldung (kommstrg. h)
description: Ruft das Handle für das Kalender Steuerelement (DTP) des untergeordneten Monats eines Datums und einer Uhrzeit Auswahl ab. Sie können diese Nachricht explizit senden oder das DateTime- \_ getmonthcal-Makro verwenden.
ms.assetid: 78bbdcc9-2b2b-420b-be9b-6f2f573d60b6
keywords:
- Windows-Steuerelemente für DTM_GETMONTHCAL Meldung
topic_type:
- apiref
api_name:
- DTM_GETMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99609ed3a437990889066da9a3424ef147c3d6b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956831"
---
# <a name="dtm_getmonthcal-message"></a>DTM \_ getmonthcal-Nachricht

Ruft das Handle für das Kalender Steuerelement (DTP) des untergeordneten Monats eines Datums und einer Uhrzeit Auswahl ab. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ getmonthcal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Steuerelement des untergeordneten Monats Kalenders des DTP-Steuer Elements zurück, wenn erfolgreich, andernfalls **null** .

## <a name="remarks"></a>Bemerkungen

DTP-Steuerelemente erstellen ein untergeordnetes Monatskalender-Steuerelement, wenn der Benutzer auf den Dropdown Pfeil klickt ([Dtn- \_ Dropdown](dtn-dropdown.md) Benachrichtigung). Wenn der Monatskalender nicht mehr benötigt wird, wird er zerstört (eine [Dtn- \_ closeup](dtn-closeup.md) -Benachrichtigung wird bei der Zerstörung gesendet). Daher darf Ihre Anwendung nicht auf ein statisches Handle für den untergeordneten Monatskalender des DTP-Steuer Elements zurückgreifen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[DTN- \_ Schließung](dtn-closeup.md)
</dt> <dt>

[DTN- \_ Dropdown](dtn-dropdown.md)
</dt> </dl>

 

 





