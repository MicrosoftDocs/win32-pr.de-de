---
title: MCM_SETMAXSELCOUNT (Commctrl.h)
description: Legt die maximale Anzahl von Tagen fest, die in einem Monatskalender-Steuerelement ausgewählt werden können. Sie können diese Nachricht explizit oder mithilfe des \_ MonthCal-Makros SetMaxSelCount senden.
ms.assetid: 190453ab-e53b-4db7-82c1-f9d50188ad39
keywords:
- MCM_SETMAXSELCOUNT von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- MCM_SETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 491e28f9af1e01a97ccbdb0d2928d35117939b82d9acc1e91ea8078aae337bcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078974"
---
# <a name="mcm_setmaxselcount-message"></a>MCM \_ SETMAXSELCOUNT-Meldung

Legt die maximale Anzahl von Tagen fest, die in einem Monatskalender-Steuerelement ausgewählt werden können. Sie können diese Nachricht explizit oder mithilfe des [**\_ MonthCal-Makros SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Wert vom **Typ int,** der auf die maximale Anzahl von Tagen festgelegt wird, die ausgewählt werden können.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück. Diese Meldung wird nicht angezeigt, wenn sie auf ein Monatskalender-Steuerelement angewendet wird, das nicht das [**MCS \_ MULTISELECT-Format**](month-calendar-control-styles.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





