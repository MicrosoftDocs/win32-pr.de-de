---
title: PGM_SETBKCOLOR (Commctrl.h)
description: Legt die aktuelle Hintergrundfarbe für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das \_ Pager-Makro SetBkColor verwenden.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- PGM_SETBKCOLOR meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d727bf401fae3b8c58b96fe8b5190a3ad427abb40b0478d59de087add553ddf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830181"
---
# <a name="pgm_setbkcolor-message"></a>PGM \_ SETBKCOLOR-Meldung

Legt die aktuelle Hintergrundfarbe für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**\_ Pager-Makro SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

**COLORREF-Wert,** der die neue Hintergrundfarbe des Pager-Steuerelements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **COLORREF-Wert** zurück, der die vorherige Hintergrundfarbe enthält.

## <a name="remarks"></a>Hinweise

Standardmäßig verwendet das Pager-Steuerelement die Gesichtsfarbe der Systemschaltfläche als Hintergrundfarbe. Dies ist die gleiche Farbe, die durch Aufrufen von [**GetSysColorBrush mit**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) COLOR \_ BTNFACE abgerufen werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

