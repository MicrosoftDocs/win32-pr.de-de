---
title: TDM_ENABLE_RADIO_BUTTON Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert ein Optionsfeld in einem Aufgaben Dialogfeld.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- Windows-Steuerelemente für TDM_ENABLE_RADIO_BUTTON Meldung
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
ms.openlocfilehash: a78445158c5edc920eb329cdfc52d44f9cb7d6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957098"
---
# <a name="tdm_enable_radio_button-message"></a>TDM-Optionsfeld \_ \_ \_ Nachricht aktivieren

Aktiviert oder deaktiviert ein Optionsfeld in einem Aufgaben Dialogfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein **int** -Wert, der die ID des Options Felds angibt, das aktiviert oder deaktiviert werden soll.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Gibt den Schaltflächen Zustand an. Auf 0 festlegen, um die Schaltfläche zu deaktivieren. Legen Sie auf ungleich NULL fest, um die Schaltfläche zu aktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





