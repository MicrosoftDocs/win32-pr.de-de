---
title: TDM_CLICK_VERIFICATION (Commctrl.h)
description: Simuliert einen Klick auf das Überprüfungskontrollkästchen eines Aufgabendialogfelds, sofern vorhanden.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- TDM_CLICK_VERIFICATION meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3cda5e85b138225d69e159792cbe641122e91bf9602b3e0f5edafa419edc3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876090"
---
# <a name="tdm_click_verification-message"></a>TDM CLICK \_ \_ VERIFICATION message

Simuliert einen Klick auf das Überprüfungskontrollkästchen eines Aufgabendialogfelds, sofern vorhanden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

**TRUE,** um den Status des zu aktivierenden Kontrollkästchens zu festlegen; **FALSE,** um die Option so zu deaktivieren, dass sie deaktiviert wird.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

**TRUE,** um den Tastaturfokus auf das Kontrollkästchen zu setzen; **Andernfalls FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





