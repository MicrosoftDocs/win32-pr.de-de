---
title: DTM_SETMCFONT Meldung (kommstrg. h)
description: Legt die Schriftart fest, die vom untergeordneten Monatskalender-Steuerelement des Steuer Elements für die Datums-und Uhrzeit Auswahl verwendet werden soll. Sie können diese Nachricht explizit senden oder das DateTime- \_ SetMonthCalFont-Makro verwenden.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- Windows-Steuerelemente für DTM_SETMCFONT Meldung
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
ms.openlocfilehash: b148ffb95acd82257265bf0bab53000b10803793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477931"
---
# <a name="dtm_setmcfont-message"></a>DTM- \_ Nachricht

Legt die Schriftart fest, die vom untergeordneten Monatskalender-Steuerelement des Steuer Elements für die Datums-und Uhrzeit Auswahl verwendet werden soll. Sie können diese Nachricht explizit senden oder das [**DateTime- \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Handle für die Schriftart, die festgelegt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt an, ob das Steuerelement sofort nach dem Festlegen der Schriftart neu gezeichnet werden soll. Wenn Sie diesen Parameter auf " **true** " festlegen, wird das Steuerelement neu gezeichnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Nachricht wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





