---
title: HDM_SETIMAGELIST Meldung (kommstrg. h)
description: Weist einem vorhandenen Header Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit senden oder den Header \_ SetImageList oder das \_ setstateimagelist-Makro des Headers verwenden.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- Windows-Steuerelemente für HDM_SETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949819"
---
# <a name="hdm_setimagelist-message"></a>HDM \_ SetImageList-Meldung

Weist einem vorhandenen Header Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit senden oder den [**Header \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) oder das [**\_ setstateimagelist**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) -Makro des Headers verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>*wParam*</dt> <dd>Einer der folgenden Werte:

| Wert                                                                                                                                                      | Bedeutung                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**hdsil \_ Normal**</dt> </dl> | Gibt an, dass es sich hierbei um eine normale Bildliste handelt.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**hdsil- \_ Status**</dt> </dl>    | Gibt an, dass es sich um eine Status Bild Liste handelt.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für eine Bildliste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, die dem Steuerelement zuvor zugeordnet ist. Gibt bei einem Fehler **null** zurück oder, wenn zuvor keine Bildliste festgelegt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





