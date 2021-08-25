---
title: DTM_SETMCSTYLE Nachricht (Commctrl.h)
description: Legt den Stil eines DTP-Steuerelements (Date and Time Picker) fest. Senden Sie diese Nachricht explizit oder mithilfe des \_ DateTime-Makros SetMonthCalStyle.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- DTM_SETMCSTYLE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 2805f2213bcbb1fa91a10ea80005b8b23bbc7447973bba6930bfdcb1e52a9e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877800"
---
# <a name="dtm_setmcstyle-message"></a>FEHLERMELDUNG \_ SETMCSTYLE

Legt den Stil eines DTP-Steuerelements (Date and Time Picker) fest. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ DateTime-Makros SetMonthCalStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>Ein Stilwert. Weitere Informationen finden Sie unter <a href="month-calendar-control-styles.md">Monatskalender-Steuerelementstile.</a></dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert des vorherigen Stils zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





