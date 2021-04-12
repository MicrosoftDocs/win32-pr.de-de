---
title: TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE Meldung (kommstrg. h)
description: Gibt an, ob eine angegebene Aufgaben Dialogfeld-oder Befehls Verknüpfung über ein Schild Symbol der Benutzerkontensteuerung (UAC) verfügen soll. Das heißt, ob für die von der Schaltfläche aufgerufene Aktion eine Erhöhung erforderlich ist.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- Windows-Steuerelemente für TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE Meldung
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5f8479e88a3b63cbd5fab6a5686913864fd9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105974"
---
# <a name="tdm_set_button_elevation_required_state-message"></a>TDM \_ - \_ Schaltflächen Erweiterung \_ \_ erforderliche \_ Zustands Meldung

Gibt an, ob eine angegebene Aufgaben Dialogfeld-oder Befehls Verknüpfung über ein Schild Symbol der Benutzerkontensteuerung (UAC) verfügen soll. Das heißt, ob für die von der Schaltfläche aufgerufene Aktion eine Erhöhung erforderlich ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Die ID der zu aktualisierenden pushschaltfläche oder des Befehls Links.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Legen Sie den Wert auf 0 fest, um anzugeben, dass die von der Schaltfläche aufgerufene Aktion keine Erhöhung erfordert. Legen Sie auf ungleich NULL fest, um anzugeben, dass die Aktion eine Erhöhung erfordert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





