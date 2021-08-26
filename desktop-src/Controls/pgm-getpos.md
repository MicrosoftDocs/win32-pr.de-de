---
title: PGM_GETPOS (Commctrl.h)
description: Ruft die aktuelle Bildlaufposition des Pager-Steuerelements ab. Sie können diese Nachricht explizit senden oder das Pager \_ GetPos-Makro verwenden.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- PGM_GETPOS message Windows Controls
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f1d5608b720d5a5d3d661a368d094da9469d71108874a6cec5495bf120cc54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046870"
---
# <a name="pgm_getpos-message"></a>PGM \_ GETPOS-Nachricht

Ruft die aktuelle Bildlaufposition des Pager-Steuerelements ab. Sie können diese Nachricht explizit senden oder das [**Pager \_ GetPos-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen INT-Wert zurück, der die aktuelle Bildlaufposition in Pixel enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





