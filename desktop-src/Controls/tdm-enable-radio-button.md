---
title: TDM_ENABLE_RADIO_BUTTON Meldung (Commctrl.h)
description: Aktiviert oder deaktiviert ein Optionsfeld in einem Aufgabendialogfeld.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- TDM_ENABLE_RADIO_BUTTON Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TDM_ENABLE_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493c6813f15baa3ad3b5ceb7050049f620010a9eed12d75d09b3c9f102aa62db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876071"
---
# <a name="tdm_enable_radio_button-message"></a>TDM \_ ENABLE RADIO BUTTON \_ \_ message

Aktiviert oder deaktiviert ein Optionsfeld in einem Aufgabendialogfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Ein **int-Wert,** der die ID des Optionsfelds angibt, das aktiviert oder deaktiviert werden soll.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Gibt den Schaltflächenzustand an. Legen Sie auf 0 fest, um die Schaltfläche zu deaktivieren. legen Sie auf ungleich 0 (null) fest, um die Schaltfläche zu aktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





