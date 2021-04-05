---
title: TDM_SET_PROGRESS_BAR_RANGE Meldung (kommstrg. h)
description: Legt die minimalen und maximalen Werte für die Statusanzeige in einem Aufgaben Dialogfeld fest.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- Windows-Steuerelemente für TDM_SET_PROGRESS_BAR_RANGE Meldung
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859290"
---
# <a name="tdm_set_progress_bar_range-message"></a>TDM \_ - \_ Meldung "Statusanzeige \_ \_ Bereich festlegen"

Legt die minimalen und maximalen Werte für die Statusanzeige in einem Aufgaben Dialogfeld fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Muss Null sein.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den Mindestwert an. Standardmäßig ist der Minimalwert 0 (null). Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den maximalen Wert an. Standardmäßig ist der Höchstwert 100.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den vorherigen minimalen und maximalen Wert zurück, wenn erfolgreich, andernfalls 0 (null). Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den minimalen Wert, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält den maximalen Wert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

