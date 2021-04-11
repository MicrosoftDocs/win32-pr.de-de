---
title: TDM_SET_MARQUEE_PROGRESS_BAR Meldung (kommstrg. h)
description: Gibt an, ob die gehostete Statusanzeige eines Aufgaben Dialogfelds im Marquee-Modus angezeigt werden soll.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- Windows-Steuerelemente für TDM_SET_MARQUEE_PROGRESS_BAR Meldung
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105969"
---
# <a name="tdm_set_marquee_progress_bar-message"></a>TDM \_ Set \_ Marquee \_ - \_ Statusanzeige Meldung

Gibt an, ob die gehostete Statusanzeige eines Aufgaben Dialogfelds im Marquee-Modus angezeigt werden soll.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein **boolescher** Wert, der angibt, ob die Statusanzeige im Marquee-Modus angezeigt werden soll. Der Wert **true** wechselt im Marquee-Modus, und der Wert **false** schaltet den Marquee-Modus um.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Bemerkungen

Informationen zum Marquee-Modus finden Sie unter Statusanzeige- [Steuer](progress-bar-control.md)Element.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





