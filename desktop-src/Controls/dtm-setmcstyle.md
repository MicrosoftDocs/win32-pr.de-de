---
title: DTM_SETMCSTYLE Meldung (kommstrg. h)
description: Legt den Stil eines Steuer Elements für die Datums-und Zeitauswahl fest. Senden Sie diese Nachricht explizit oder mithilfe des DateTime- \_ setmonthcalstyle-Makros.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- Windows-Steuerelemente für DTM_SETMCSTYLE Meldung
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104840"
---
# <a name="dtm_setmcstyle-message"></a>DTM- \_ ltmcstyle-Nachricht

Legt den Stil eines Steuer Elements für die Datums-und Zeitauswahl fest. Senden Sie diese Nachricht explizit oder mithilfe des [**DateTime- \_ setmonthcalstyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>Ein-Stilwert. Weitere Informationen finden Sie unter <a href="month-calendar-control-styles.md">Month Calendar Control Styles</a>.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert des vorherigen Stils zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





