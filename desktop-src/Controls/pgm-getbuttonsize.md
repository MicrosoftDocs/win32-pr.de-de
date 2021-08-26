---
title: PGM_GETBUTTONSIZE (Commctrl.h)
description: Ruft die aktuelle Schaltflächengröße für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das \_ Pager-Makro GetButtonSize verwenden.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- PGM_GETBUTTONSIZE message Windows Controls
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a77bbfdbac95c10afc721cfbae41798083ea98f4dd78e9dfdec9099871d7afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985899"
---
# <a name="pgm_getbuttonsize-message"></a>PGM \_ GETBUTTONSIZE-Nachricht

Ruft die aktuelle Schaltflächengröße für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**\_ Pager-Makro GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen INT-Wert zurück, der die aktuelle Schaltflächengröße in Pixel enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**PGM \_ SETBUTTONSIZE**](pgm-setbuttonsize.md)
</dt> </dl>

 

 





