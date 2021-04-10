---
title: MCM_SETCURRENTVIEW Meldung (kommstrg. h)
description: Legt die aktuelle Ansicht des Kalenders fest. Sie können diese Nachricht explizit oder mit dem monthcal \_ SetCurrentView-Makro senden.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- Windows-Steuerelemente für MCM_SETCURRENTVIEW Meldung
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d383c984932c19805f452cb39841c2edf36809b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957104"
---
# <a name="mcm_setcurrentview-message"></a>MCM \_ SetCurrentView-Nachricht

Legt die aktuelle Ansicht des Kalenders fest. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ SetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Neue Ansicht. Eine der folgenden Konstanten.



| Wert                                                                                                                                                      | Bedeutung                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <dt>**mcmv- \_ Monat**</dt> </dl>       | Monatliche Ansicht.<br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <dt>**mcmv- \_ Jahr**</dt> </dl>          | Jährliche Ansicht.<br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <dt>**mcmv- \_ Jahrzehnt**</dt> </dl>    | Dekade-Ansicht.<br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <dt>**mcmv \_ Jahrhundert**</dt> </dl> | Jahrhundert Ansicht.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





