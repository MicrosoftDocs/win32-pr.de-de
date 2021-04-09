---
title: TDM_SET_PROGRESS_BAR_MARQUEE Meldung (kommstrg. h)
description: Startet und beendet die Marquee-Anzeige der Statusanzeige in einem Aufgaben Dialogfeld und legt die Geschwindigkeit des Marquee fest.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- Windows-Steuerelemente für TDM_SET_PROGRESS_BAR_MARQUEE Meldung
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
ms.openlocfilehash: 2f73d3d4308d2e3f963c015b6e36f385902bea6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040944"
---
# <a name="tdm_set_progress_bar_marquee-message"></a>TDM \_ Festlegen der Statusanzeige- \_ \_ \_ Marquee-Nachricht

Startet und beendet die Marquee-Anzeige der Statusanzeige in einem Aufgaben Dialogfeld und legt die Geschwindigkeit des Marquee fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein **boolescher** Wert, der angibt, ob die Marquee-Anzeige ein-oder ausgeschaltet werden soll. Verwenden Sie **true** , um die Marquee-Anzeige zu aktivieren, oder **false** , um Sie zu deaktivieren.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Ein **uint** , der die Zeit in Millisekunden zwischen den Marquee-Animations Aktualisierungen angibt. Wenn dieser Parameter 0 (null) ist, wird die Marquee-Animation alle 30 Millisekunden aktualisiert.

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



 

 





