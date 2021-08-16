---
title: PBM_SETBARCOLOR (Commctrl.h)
description: Legt die Farbe der Statusanzeige im Statusanzeige-Steuerelement fest.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- PBM_SETBARCOLOR meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babff5ad74d943d64f5ad61354447498e91e1325c99c82b32183fbc62eabafdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830201"
---
# <a name="pbm_setbarcolor-message"></a>PBM \_ SETBARCOLOR-Meldung

Legt die Farbe der Statusanzeige im Statusanzeige-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Der **COLORREF-Wert,** der die neue Statusanzeigenfarbe angibt. Die Angabe des CLR \_ DEFAULT-Werts bewirkt, dass die Statusanzeige ihre Standardfarbe für die Statusanzeige verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die vorherige Statusanzeigenfarbe oder CLR DEFAULT zurück, wenn \_ die Statusanzeigefarbe die Standardfarbe ist.

## <a name="remarks"></a>Hinweise

Wenn visuelle Stile aktiviert sind, hat diese Meldung keine Auswirkungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





