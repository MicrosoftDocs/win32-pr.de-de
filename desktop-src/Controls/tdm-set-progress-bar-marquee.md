---
title: TDM_SET_PROGRESS_BAR_MARQUEE Meldung (Commctrl.h)
description: Startet und beendet die Festzeltanzeige der Statusanzeige in einem Aufgabendialogfeld und legt die Geschwindigkeit des Festzeltes fest.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- TDM_SET_PROGRESS_BAR_MARQUEE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b92816b70e683b9f58e0de2247b2710da38bee891caa39d9026fc342168c6be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060650"
---
# <a name="tdm_set_progress_bar_marquee-message"></a>TDM \_ SET PROGRESS BAR \_ \_ \_ MARQUEE message

Startet und beendet die Festzeltanzeige der Statusanzeige in einem Aufgabendialogfeld und legt die Geschwindigkeit des Festzeltes fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Eine **BOOL,** die angibt, ob die Marquee-Anzeige ein- oder ausgeschaltet werden soll. Verwenden Sie **TRUE,** um die Marquee-Anzeige zu aktivieren, oder **FALSE,** um sie zu deaktivieren.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Ein **UINT,** der die Zeit in Millisekunden zwischen Aktualisierungen der Markquee-Animation angibt. Wenn dieser Parameter 0 (null) ist, wird die Marquee-Animation alle 30 Millisekunden aktualisiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="remarks"></a>Hinweise

Informationen zum Marquee-Modus finden Sie unter [Statusleisten-Steuerelement.](progress-bar-control.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





