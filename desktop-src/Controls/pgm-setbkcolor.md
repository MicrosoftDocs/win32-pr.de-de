---
title: PGM_SETBKCOLOR Meldung (kommstrg. h)
description: Legt die aktuelle Hintergrundfarbe für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das Pager- \_ SetBkColor-Makro verwenden.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- Windows-Steuerelemente für PGM_SETBKCOLOR Meldung
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
ms.openlocfilehash: fa9e8dc1c0cad3e60bdde3f3c05d77d8c57b98ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103479"
---
# <a name="pgm_setbkcolor-message"></a>PGM- \_ SetBkColor-Nachricht

Legt die aktuelle Hintergrundfarbe für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**Pager- \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

**COLORREF** -Wert, der die neue Hintergrundfarbe des Pager-Steuer Elements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **COLORREF** -Wert zurück, der die vorherige Hintergrundfarbe enthält.

## <a name="remarks"></a>Bemerkungen

Standardmäßig verwendet das Pager-Steuerelement die Vordergrundfarbe der System Schaltfläche als Hintergrundfarbe. Dies ist die gleiche Farbe, die durch den Aufruf von [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) mit Color \_ btnface abgerufen werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

