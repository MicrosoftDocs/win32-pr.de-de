---
title: MCM_SETCALENDARBORDER (Commctrl.h)
description: Legt die Größe des Rahmens in Pixel fest. Sie können diese Nachricht explizit oder mithilfe des \_ MonthCal-Makros SetCalendarBorder senden.
ms.assetid: 2a64a08f-a1fb-47a8-8f09-725807e87a03
keywords:
- MCM_SETCALENDARBORDER meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- MCM_SETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e020ad282ce21555e6c3a74198a0034013ac1d7cfac8f4eb68e52137e5f684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697200"
---
# <a name="mcm_setcalendarborder-message"></a>MCM \_ SETCALENDARBORDER-Meldung

Legt die Größe des Rahmens in Pixel fest. Sie können diese Nachricht explizit oder mithilfe des [**\_ MonthCal-Makros SetCalendarBorder**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcalendarborder) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

True **gibt** an, dass die Rahmengröße auf die Anzahl von Pixeln festgelegt wird, die *lParam* angibt. False **gibt** an, dass die Rahmengröße auf den vom Design angegebenen Standardwert zurückgesetzt wird, oder null, wenn keine Designs verwendet werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Anzahl der Pixel der Rahmengröße.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





