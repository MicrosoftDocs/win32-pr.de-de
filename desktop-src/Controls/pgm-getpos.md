---
title: PGM_GETPOS Meldung (kommstrg. h)
description: Ruft die aktuelle Bild Lauf Position des Pager-Steuer Elements ab. Sie können diese Nachricht explizit senden oder das Pager- \_ GetPos-Makro verwenden.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- Windows-Steuerelemente für PGM_GETPOS Meldung
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
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344485"
---
# <a name="pgm_getpos-message"></a>PGM- \_ GetPos-Nachricht

Ruft die aktuelle Bild Lauf Position des Pager-Steuer Elements ab. Sie können diese Nachricht explizit senden oder das [**Pager- \_ GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen int-Wert zurück, der die aktuelle Bild Lauf Position in Pixel enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





