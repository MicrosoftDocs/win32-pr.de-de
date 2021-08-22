---
title: MCM_GETMONTHRANGE (Commctrl.h)
description: Ruft Datumsinformationen ab (unter Verwendung von SYSTEMTIME-Strukturen), die die hohen und niedrigen Grenzwerte der Anzeige eines Monatskalender-Steuerelements darstellt. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ GetMonthRange-Makros senden.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- MCM_GETMONTHRANGE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc55f9732199f2e6e031248003c6dcad4abe8cb713182081666cfbee6a4ce50b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319580"
---
# <a name="mcm_getmonthrange-message"></a>MCM \_ GETMONTHRANGE-Nachricht

Ruft Datumsinformationen ab (unter Verwendung [**von SYSTEMTIME-Strukturen),**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die die hohen und niedrigen Grenzwerte der Anzeige eines Monatskalender-Steuerelements darstellt. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ GetMonthRange-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wert, der den Bereich der abzurufenden Bereichsgrenzwerte an gibt. Dieser Wert muss einer der folgenden sein:



| Wert                                                                                                                                                      | Bedeutung                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <dt>**GMR \_ DAYSTATE**</dt> </dl> | Schließen Sie vorhergehende und nachgehende Monate des sichtbaren Bereichs ein, die nur teilweise angezeigt werden. <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <dt>**GMR \_ VISIBLE**</dt> </dl>    | Schließen Sie nur die Monate ein, die vollständig angezeigt werden. <br/>                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Zwei-Element-Array von [**SYSTEMTIME-Strukturen,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die die untere und obere Grenze des durch *wParam angegebenen Bereichs erhalten.* Die unteren und oberen Grenzwerte werden in *lprgSysTimeArray* \[ 0 bzw. \] *lprgSysTimeArray* \[ 1 \] platziert. Dieser Parameter muss eine gültige Adresse sein und darf nicht **NULL sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen INT-Wert zurück, der den Bereich in Monaten darstellt, der von den beiden in lParam zurückgegebenen *Grenzwerten überspannt wird.*

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

 

