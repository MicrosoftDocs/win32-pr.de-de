---
title: MCM_GETMONTHDELTA (Commctrl.h)
description: Ruft die Bildlaufrate für ein Monatskalender-Steuerelement ab. Die Bildlaufrate ist die Anzahl der Monate, die das Steuerelement seine Anzeige verschiebt, wenn der Benutzer auf eine Bildlaufschaltfläche klickt. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ GetMonthDelta-Makros senden.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- MCM_GETMONTHDELTA von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13a13d75a1655c1082b4b4611517915be14e27b0fb1c5f94fb5a17f6db973e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319610"
---
# <a name="mcm_getmonthdelta-message"></a>MCM \_ GETMONTHDELTA-Nachricht

Ruft die Bildlaufrate für ein Monatskalender-Steuerelement ab. Die Bildlaufrate ist die Anzahl der Monate, die das Steuerelement seine Anzeige verschiebt, wenn der Benutzer auf eine Bildlaufschaltfläche klickt. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ GetMonthDelta-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn das Monatsdelta zuvor mithilfe der [**MCM \_ SETMONTHDELTA-Nachricht**](mcm-setmonthdelta.md) festgelegt wurde, gibt einen INT-Wert zurück, der die aktuelle Bildlaufrate des Monatskalenders darstellt. Wenn das Monatsdelta zuvor nicht mithilfe der **MCM \_ SETMONTHDELTA-Nachricht** festgelegt wurde oder das Monatsdelta auf den Standardwert zurückgesetzt wurde, gibt einen INT-Wert zurück, der die aktuelle Anzahl der sichtbaren Monate darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





