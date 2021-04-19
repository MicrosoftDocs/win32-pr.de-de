---
title: PBM_SETSTEP Meldung (kommstrg. h)
description: Gibt das Schritt Inkrement für eine Statusanzeige an. Der Schritt Inkrement ist der Betrag, um den die Statusanzeige bei jedem Empfang einer PBM-StepIt-Nachricht die aktuelle Position vergrößert \_ . Standardmäßig ist das Schritt Inkrement auf 10 festgelegt.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- Windows-Steuerelemente für PBM_SETSTEP Meldung
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1240d09aeadcd7994187704d0b5a4630ab1b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346513"
---
# <a name="pbm_setstep-message"></a>PBM- \_ SetStep-Nachricht

Gibt das Schritt Inkrement für eine Statusanzeige an. Der Schritt Inkrement ist der Betrag, um den die Statusanzeige bei jedem Empfang einer [**PBM- \_ StepIt**](pbm-stepit.md) -Nachricht die aktuelle Position vergrößert. Standardmäßig ist das Schritt Inkrement auf 10 festgelegt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Neuer Schritt Inkrement.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das vorherige Schritt Inkrement zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





