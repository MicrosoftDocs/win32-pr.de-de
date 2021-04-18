---
title: TDM_ENABLE_BUTTON Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert eine Schaltfläche "Push" in einem Aufgaben Dialogfeld.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- Windows-Steuerelemente für TDM_ENABLE_BUTTON Meldung
topic_type:
- apiref
api_name:
- TDM_ENABLE_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db10d616b4d07adcdc8c97495f7d12c89e603a7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343476"
---
# <a name="tdm_enable_button-message"></a>TDM \_ - \_ Schaltflächen Nachricht aktivieren

Aktiviert oder deaktiviert eine Schaltfläche "Push" in einem Aufgaben Dialogfeld.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein **int** -Wert, der die ID der Push-Schaltfläche angibt, die aktiviert oder deaktiviert werden soll.

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



 

 





