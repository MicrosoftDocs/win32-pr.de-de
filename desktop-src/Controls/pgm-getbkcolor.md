---
title: PGM_GETBKCOLOR Meldung (kommstrg. h)
description: Ruft die aktuelle Hintergrundfarbe für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das Pager- \_ GetBkColor-Makro verwenden.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- Windows-Steuerelemente für PGM_GETBKCOLOR Meldung
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
ms.openlocfilehash: 4b58b139dd1caafcdefc6893e2b8a5e3312d3e28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742528"
---
# <a name="pgm_getbkcolor-message"></a>PGM \_ GetBkColor-Nachricht

Ruft die aktuelle Hintergrundfarbe für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**Pager- \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **COLORREF** -Wert zurück, der die aktuelle Hintergrundfarbe enthält.

## <a name="remarks"></a>Bemerkungen

Standardmäßig verwendet das Pager-Steuerelement die Vordergrundfarbe der System Schaltfläche als Hintergrundfarbe. Dies ist die gleiche Farbe, die durch den Aufruf von [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) mit Color \_ btnface abgerufen werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

