---
title: PGM_SETPOS Meldung (kommstrg. h)
description: Legt die aktuelle Bild Lauf Position für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das Pager- \_ SetPos-Makro verwenden.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- Windows-Steuerelemente für PGM_SETPOS Meldung
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741224"
---
# <a name="pgm_setpos-message"></a>PGM- \_ SetPos-Nachricht

Legt die aktuelle Bild Lauf Position für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**Pager- \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Der Wert vom Typ " **int** ", der die neue Scrollposition enthält, in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





