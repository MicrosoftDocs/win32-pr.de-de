---
title: HDM_GETIMAGELIST (Commctrl.h)
description: Ruft das Handle für die Bildliste ab, die für ein vorhandenes Header-Steuerelement festgelegt wurde. Sie können diese Nachricht explizit senden oder das Header \_ GetImageList- oder Header \_ GetStateImageList-Makro verwenden.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- HDM_GETIMAGELIST message Windows Controls
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
ms.openlocfilehash: 8149dd4914ceb1835e9e04442492855e9c25340604ed4e4eeb2619c62b88e69f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540910"
---
# <a name="hdm_getimagelist-message"></a>HDM \_ GETIMAGELIST-Nachricht

Ruft das Handle für die Bildliste ab, die für ein vorhandenes Header-Steuerelement festgelegt wurde. Sie können diese Nachricht explizit senden oder das [**Header \_ GetImageList-**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) oder [**Header \_ GetStateImageList-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>*wParam*</dt> <dd>Einer der folgenden Werte:

| Wert                                                                                                                                                      | Bedeutung                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ NORMAL**</dt> </dl> | Gibt an, dass es sich um eine normale Bildliste handelt.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**HDSIL \_ STATE**</dt> </dl>    | Gibt an, dass es sich um eine Statusbildliste handelt.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein Handle für den Bildlistensatz für das Header-Steuerelement zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





