---
title: PBM_STEPIT Meldung (kommstrg. h)
description: Verschiebt die aktuelle Position für eine Statusanzeige um das Schritt Inkrement und zeichnet den Balken neu, um die neue Position widerzuspiegeln. Eine Anwendung legt das Schritt Inkrement fest, indem die PBM- \_ SetStep-Nachricht gesendet wird.
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- Windows-Steuerelemente für PBM_STEPIT Meldung
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956808"
---
# <a name="pbm_stepit-message"></a>PBM- \_ StepIt-Nachricht

Verschiebt die aktuelle Position für eine Statusanzeige um das Schritt Inkrement und zeichnet den Balken neu, um die neue Position widerzuspiegeln. Eine Anwendung legt das Schritt Inkrement fest, indem die [**PBM- \_ SetStep**](pbm-setstep.md) -Nachricht gesendet wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Position zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Position den maximalen Bereichs Wert überschreitet, setzt diese Nachricht die aktuelle Position zurück, sodass die Statusanzeige von Anfang an erneut beginnt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





