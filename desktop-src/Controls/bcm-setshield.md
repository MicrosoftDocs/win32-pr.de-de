---
title: BCM_SETSHIELD Meldung (kommstrg. h)
description: Legt den Status der erhöhten Rechte für eine angegebene Schaltfläche oder einen Befehls Link fest, um ein Symbol mit erhöhten Rechten anzuzeigen. Senden Sie diese Nachricht explizit oder mithilfe des Schaltflächen-Makros "" \_ .
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- Windows-Steuerelemente für BCM_SETSHIELD Meldung
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2149e2945f2876309459c287961b7b0a4a1f9acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103490"
---
# <a name="bcm_setshield-message"></a>BCM- \_ SETSHIELD-Nachricht

Legt den Status der erhöhten Rechte für eine angegebene Schaltfläche oder einen Befehls Link fest, um ein Symbol mit erhöhten Rechten anzuzeigen. Senden Sie diese Nachricht explizit oder mithilfe des [**Schalt \_**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) Flächen-Makros "".

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Ein **boolescher** Wert, der **true** ist, wenn ein Symbol mit erhöhten Rechten gezeichnet werden soll, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 1 zurück, wenn erfolgreich, oder andernfalls einen Fehlercode.

## <a name="remarks"></a>Bemerkungen

Um diese Funktionalität nutzen zu können, muss eine Anwendung für die Verwendung comctl32.dll Version 6 angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





