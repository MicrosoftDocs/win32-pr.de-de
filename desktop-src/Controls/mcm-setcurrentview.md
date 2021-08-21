---
title: MCM_SETCURRENTVIEW (Commctrl.h)
description: Legt die aktuelle Ansicht des Kalenders fest. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ SetCurrentView-Makros senden.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- MCM_SETCURRENTVIEW meldungssteuerelemente Windows
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
ms.openlocfilehash: 33cf7206fb7e778c0ab7d28ee8947b9327e8cc98bd8ae8c9063213814676a77e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019038"
---
# <a name="mcm_setcurrentview-message"></a>MCM \_ SETCURRENTVIEW-Meldung

Legt die aktuelle Ansicht des Kalenders fest. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ SetCurrentView-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview) senden.

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
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <dt>**MCMV \_ MONTH**</dt> </dl>       | Monatsansicht.<br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <dt>**MCMV \_ YEAR**</dt> </dl>          | Jahresansicht.<br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <dt>**MCMV \_ DECADE**</dt> </dl>    | Ansicht "100 Jahre".<br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <dt>**MCMV \_ CENTURY**</dt> </dl> | Century-Ansicht.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





