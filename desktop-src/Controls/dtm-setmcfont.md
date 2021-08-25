---
title: DTM_SETMCFONT (Commctrl.h)
description: Legt die Schriftart fest, die vom untergeordneten Monatskalender-Steuerelement des DTP-Steuerelements (Datums- und Uhrzeitauswahl) verwendet werden soll. Sie können diese Nachricht explizit senden oder das \_ DateTime-Makro SetMonthCalFont verwenden.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- DTM_SETMCFONT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa1b34c1a51e365868cbdae30e46cd299937d3d6fe33bad6c57d630a0b226fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877810"
---
# <a name="dtm_setmcfont-message"></a>SMS \_ SETMCFONT-Nachricht

Legt die Schriftart fest, die vom untergeordneten Monatskalender-Steuerelement des DTP-Steuerelements (Datums- und Uhrzeitauswahl) verwendet werden soll. Sie können diese Nachricht explizit senden oder das [**\_ DateTime-Makro SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für die Schriftart, die festgelegt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt an, ob das Steuerelement unmittelbar nach dem Festlegen der Schriftart neu gezeichnet werden soll. Wenn Sie diesen Parameter auf **TRUE festlegen,** wird das Steuerelement selbst neu gezeichnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Meldung wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





