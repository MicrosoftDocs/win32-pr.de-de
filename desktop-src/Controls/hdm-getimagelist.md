---
title: HDM_GETIMAGELIST Meldung (kommstrg. h)
description: Ruft das Handle für die Bildliste ab, die für ein vorhandenes Header Steuerelement festgelegt wurde. Sie können diese Nachricht explizit senden oder den Header \_ GetImageList oder das \_ getstateimagelist-Makro des Headers verwenden.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- Windows-Steuerelemente für HDM_GETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742280"
---
# <a name="hdm_getimagelist-message"></a>HDM \_ GetImageList-Meldung

Ruft das Handle für die Bildliste ab, die für ein vorhandenes Header Steuerelement festgelegt wurde. Sie können diese Nachricht explizit senden oder den [**Header \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) oder das [**\_ getstateimagelist**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) -Makro des Headers verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>*wParam*</dt> <dd>Einer der folgenden Werte:

| Wert                                                                                                                                                      | Bedeutung                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**hdsil \_ Normal**</dt> </dl> | Gibt an, dass es sich hierbei um eine normale Bildliste handelt.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**hdsil- \_ Status**</dt> </dl>    | Gibt an, dass es sich um eine Status Bild Liste handelt.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein Handle für die Bildliste zurück, die für das Header Steuerelement festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





