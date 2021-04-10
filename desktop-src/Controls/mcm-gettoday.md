---
title: MCM_GETTODAY Meldung (kommstrg. h)
description: Ruft die Datumsinformationen für das Datum ab, das als \ 0034; heute \ 0034; angegeben ist. für ein Monatskalender-Steuerelement. Sie können diese Nachricht explizit oder mit dem monthcal \_ gettoday-Makro senden.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- Windows-Steuerelemente für MCM_GETTODAY Meldung
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
ms.openlocfilehash: 21538af3c573b3d972b7f16bfe024e0d36211644
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956539"
---
# <a name="mcm_gettoday-message"></a>MCM \_ gettoday-Meldung

Ruft die Datumsinformationen für das als "heute" angegebene Datum für ein Monatskalender-Steuerelement ab. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ gettoday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur, die die Datumsinformationen empfängt. Dieser Parameter muss eine gültige Adresse sein und darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Uhrzeiten im Monatskalender-Steuerelement](month-calendar-controls.md)
</dt> </dl>

 

