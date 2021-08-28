---
title: MCM_SETRANGE (Commctrl.h)
description: Legt die minimalen und maximalen zulässigen Datumsangaben für ein Monatskalender-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ SetRange-Makros senden.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- MCM_SETRANGE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c66e9cca17aabd93bfba896d361da6b90eab0c5c21fc4d50ec3c81a9eba5ccd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319250"
---
# <a name="mcm_setrange-message"></a>MCM \_ SETRANGE-Nachricht

Legt die minimalen und maximalen zulässigen Datumsangaben für ein Monatskalender-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ SetRange-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flagwerte, die angeben, welche Datumsgrenzwerte festgelegt werden. Dieser Wert muss eine oder beide der folgenden Werte haben:



| Wert                                                                                                                                          | Bedeutung                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ MAX**</dt> </dl> | Das maximal zulässige Datum wird festgelegt. Die [**SYSTEMTIME-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) bei *lpSysTimeArray* \[ 1 muss \] Datumsinformationen enthalten. <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ MIN**</dt> </dl> | Das zulässige Mindestdatum wird festgelegt. Die [**SYSTEMTIME-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) *bei lpSysTimeArray* \[ 0 muss \] Datumsinformationen enthalten. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Zwei-Element-Array von [**SYSTEMTIME-Strukturen,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die die Datumsgrenzen enthalten. Der maximale Grenzwert muss in *lpSysTimeArray* 1 sein, wenn GDTR MAX angegeben ist, und \[ \] \_ *lpSysTimeArray* 0 muss den Mindestgrenzwert enthalten, wenn GDTR MIN angegeben \[ \] \_ wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Zeiten im Monatskalender-Steuerelement](month-calendar-controls.md)
</dt> </dl>

 

