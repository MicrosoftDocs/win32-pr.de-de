---
title: CBEM_SETIMAGELIST (Commctrl.h)
description: Legt eine Bildliste für ein ComboBoxEx-Steuerelement fest.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- CBEM_SETIMAGELIST der Windows Steuerelemente
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
ms.openlocfilehash: fbd83336d27bf8e47900554a6f3c36d2d767e5e8ddd4b8680b50050d87da79bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699260"
---
# <a name="cbem_setimagelist-message"></a>CBEM \_ SETIMAGELIST-Nachricht

Legt eine Bildliste für ein ComboBoxEx-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für die Bildliste, die für das Steuerelement festgelegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, die dem Steuerelement zuvor zugeordnet war, oder gibt **NULL** zurück, wenn zuvor keine Bildliste festgelegt wurde.

## <a name="remarks"></a>Hinweise

> [!IMPORTANT]
> Die Höhe der Bilder in der Bildliste kann die Größenanforderungen des ComboBoxEx-Steuerelements ändern. Es wird empfohlen, die Größe des Steuerelements nach dem Senden dieser Meldung zu ändern, um sicherzustellen, dass es ordnungsgemäß angezeigt wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





