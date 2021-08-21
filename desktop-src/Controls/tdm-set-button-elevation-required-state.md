---
title: TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE (Commctrl.h)
description: Gibt an, ob ein bestimmtes Aufgabendialogfeld oder ein Befehlslink ein Schildsymbol für die Benutzerkontensteuerung (User Account Control, UAC) haben soll. Das heißt, ob für die von der Schaltfläche aufgerufene Aktion eine Erhöhung erforderlich ist.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE von Windows-Steuerelementen
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
ms.openlocfilehash: 2c69998da085a74b144179a0a4244c787cd3a871d63eca1e5df9c4e555b1a7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104620"
---
# <a name="tdm_set_button_elevation_required_state-message"></a>TDM \_ SET BUTTON ELEVATION REQUIRED STATE \_ \_ \_ \_ message

Gibt an, ob ein bestimmtes Aufgabendialogfeld oder ein Befehlslink ein Schildsymbol für die Benutzerkontensteuerung (User Account Control, UAC) haben soll. Das heißt, ob für die von der Schaltfläche aufgerufene Aktion eine Erhöhung erforderlich ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Die ID der zu aktualisierenden Pushschaltfläche oder des Befehlslinks.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Legen Sie auf 0 fest, um zu bestimmen, dass für die von der Schaltfläche aufgerufene Aktion keine Erhöhung erforderlich ist. Legen Sie auf ungleich 0 fest, um zu bestimmen, dass für die Aktion eine Erhöhung erforderlich ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





