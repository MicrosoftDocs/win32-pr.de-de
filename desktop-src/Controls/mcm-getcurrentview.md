---
title: MCM_GETCURRENTVIEW Meldung (Commctrl.h)
description: Ruft die aktuelle Ansicht des Kalenders ab. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ GetCurrentView-Makros senden.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- MCM_GETCURRENTVIEW Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 50f7fce3c1a22ec14ec34e849bd2e3fc4634118b11613913da4e6fae0b9b7b51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319680"
---
# <a name="mcm_getcurrentview-message"></a>MCM \_ GETCURRENTVIEW-Nachricht

Ruft die aktuelle Ansicht des Kalenders ab. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ GetCurrentView-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) senden.

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
| <dl> <dt>**MCMV \_ MONTH**</dt> </dl>   | Monatliche Ansicht.<br/> |
| <dl> <dt>**MCMV \_ YEAR**</dt> </dl>    | Jährliche Ansicht.<br/>  |
| <dl> <dt>**MCMV \_ DECADE**</dt> </dl>  | Ansicht "10 Jahre".<br/>  |
| <dl> <dt>**MCMV \_ CENTURY**</dt> </dl> | Jahrhundertansicht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





