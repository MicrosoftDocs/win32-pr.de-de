---
title: CBEM_SETIMAGELIST Meldung (kommstrg. h)
description: Legt eine Bildliste für ein ComboBoxEx-Steuerelement fest.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- Windows-Steuerelemente für CBEM_SETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957109"
---
# <a name="cbem_setimagelist-message"></a>CBEM \_ SetImageList-Meldung

Legt eine Bildliste für ein ComboBoxEx-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für die Bildliste, die für das-Steuerelement festgelegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, die dem Steuerelement zuvor zugeordnet ist, oder gibt **null** zurück, wenn zuvor keine Bildliste festgelegt wurde.

## <a name="remarks"></a>Bemerkungen

> [!IMPORTANT]
> Die Höhe der Bilder in der Bildliste kann die Größenanforderungen des ComboBoxEx-Steuer Elements ändern. Es wird empfohlen, die Größe des Steuer Elements nach dem Senden dieser Nachricht zu ändern, um sicherzustellen, dass Sie ordnungsgemäß angezeigt wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





