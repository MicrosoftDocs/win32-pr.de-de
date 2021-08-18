---
title: MCM_GETTODAY (Commctrl.h)
description: Ruft die Datumsinformationen für das als \ 0034;today \ 0034 angegebene Datum ab. für ein Monatskalender-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des MonthCal \_ GetToday-Makros senden.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- MCM_GETTODAY meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6925ff24a2d3e042a4f2c752d87642f74345116fc5cc7f94e00e811d453be4fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019028"
---
# <a name="mcm_gettoday-message"></a>MCM \_ GETTODAY-Nachricht

Ruft die Datumsinformationen für das Datum ab, das als "today" für ein Monatskalender-Steuerelement angegeben ist. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ GetToday-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**SYSTEMTIME-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) die die Datumsinformationen erhält. Dieser Parameter muss eine gültige Adresse sein und darf nicht **NULL sein.**

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

 

