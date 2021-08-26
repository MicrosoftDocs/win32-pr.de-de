---
title: PGM_GETBKCOLOR (Commctrl.h)
description: Ruft die aktuelle Hintergrundfarbe für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das \_ Pager-Makro GetBkColor verwenden.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- PGM_GETBKCOLOR message Windows Controls
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff3ee3a4be09a948654d337a47eecdd2a7b15d16b0602016aa99500cd1c3728c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985940"
---
# <a name="pgm_getbkcolor-message"></a>PGM \_ GETBKCOLOR-Nachricht

Ruft die aktuelle Hintergrundfarbe für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**\_ Pager-Makro GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **COLORREF-Wert** zurück, der die aktuelle Hintergrundfarbe enthält.

## <a name="remarks"></a>Hinweise

Standardmäßig verwendet das Pager-Steuerelement die Gesichtsfarbe der Systemschaltfläche als Hintergrundfarbe. Dies ist die gleiche Farbe, die durch Aufrufen von [**GetSysColorBrush mit**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) COLOR \_ BTNFACE abgerufen werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

