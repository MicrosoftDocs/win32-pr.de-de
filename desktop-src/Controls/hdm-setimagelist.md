---
title: HDM_SETIMAGELIST (Commctrl.h)
description: Weist einem vorhandenen Headersteuer steuerelement eine Bildliste zu. Sie können diese Nachricht explizit senden oder das Makro \_ Header SetImageList oder Header \_ SetStateImageList verwenden.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- HDM_SETIMAGELIST von Windows-Steuerelementen
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
ms.openlocfilehash: 2034a6880721914961b3bd75907df2e7b4e53360ccb3b10162f238068d85031d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435810"
---
# <a name="hdm_setimagelist-message"></a>HDM \_ SETIMAGELIST-Nachricht

Weist einem vorhandenen Headersteuer steuerelement eine Bildliste zu. Sie können diese Nachricht explizit senden oder das [**Makro \_ Header SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) oder [**Header \_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>*wParam*</dt> <dd>Einer der folgenden Werte:

| Wert                                                                                                                                                      | Bedeutung                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ NORMAL**</dt> </dl> | Gibt an, dass es sich um eine normale Bildliste handelt.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**HDSIL \_ STATE**</dt> </dl>    | Gibt an, dass es sich um eine Statusbildliste handelt.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für eine Bildliste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, die dem Steuerelement zuvor zugeordnet war. Gibt **NULL zurück,** wenn ein Fehler auft ist oder wenn zuvor keine Bildliste festgelegt wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





