---
title: PGM_SETPOS (Commctrl.h)
description: Legt die aktuelle Bildlaufposition für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das Pager \_ SetPos-Makro verwenden.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- PGM_SETPOS der Windows Steuerelemente
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
ms.openlocfilehash: a7a056d55d0ec70b3ff3068580c1e9923b363efa15e9ab26bf8aa67f476cc147
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046830"
---
# <a name="pgm_setpos-message"></a>PGM \_ SETPOS-Meldung

Legt die aktuelle Bildlaufposition für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**Pager \_ SetPos-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Der Wert vom Typ **int,** der die neue Bildlaufposition in Pixel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





