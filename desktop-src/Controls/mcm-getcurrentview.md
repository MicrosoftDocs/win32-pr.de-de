---
title: MCM_GETCURRENTVIEW Meldung (kommstrg. h)
description: Ruft die aktuelle Ansicht des Kalenders ab. Sie können diese Nachricht explizit oder mit dem monthcal \_ getcurrentview-Makro senden.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- Windows-Steuerelemente für MCM_GETCURRENTVIEW Meldung
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebbd6a2b33043294b64b8b65308520b52dbe449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478492"
---
# <a name="mcm_getcurrentview-message"></a>MCM \_ getcurrentview-Meldung

Ruft die aktuelle Ansicht des Kalenders ab. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getcurrentview**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Aktuelle Ansicht. Einer der folgenden Werte.



| Rückgabecode                                                                                  | Beschreibung              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**mcmv- \_ Monat**</dt> </dl>   | Monatliche Ansicht.<br/> |
| <dl> <dt>**mcmv- \_ Jahr**</dt> </dl>    | Jährliche Ansicht.<br/>  |
| <dl> <dt>**mcmv- \_ Jahrzehnt**</dt> </dl>  | Dekade-Ansicht.<br/>  |
| <dl> <dt>**mcmv \_ Jahrhundert**</dt> </dl> | Jahrhundert Ansicht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





