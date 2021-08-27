---
title: PGM_SETBUTTONSIZE Nachricht (Commctrl.h)
description: Legt die aktuelle Schaltflächengröße für das Pagersteuerelement fest. Sie können diese Nachricht explizit senden oder das \_ Pager-Makro SetButtonSize verwenden.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- PGM_SETBUTTONSIZE Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b120ed4bd6b7090621e09dd24b9e6a23b037fb5aed83e7ac6fc43254393330e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046790"
---
# <a name="pgm_setbuttonsize-message"></a>PGM \_ SETBUTTONSIZE-Nachricht

Legt die aktuelle Schaltflächengröße für das Pagersteuerelement fest. Sie können diese Nachricht explizit senden oder das [**\_ Pager-Makro SetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Wert vom Typ **int,** der die neue Schaltflächengröße in Pixel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **int-Wert zurück,** der die vorherige Schaltflächengröße in Pixel enthält.

## <a name="remarks"></a>Hinweise

Wenn das Pagersteuerelement den [**PGS \_ HORZ-Stil**](pager-control-styles.md) aufweist, bestimmt die Schaltflächengröße die Breite der Pagerschaltflächen. Wenn das Pagersteuerelement über den [**\_ PGS-VERT-Stil**](pager-control-styles.md) verfügt, bestimmt die Schaltflächengröße die Höhe der Pagerschaltflächen. Standardmäßig legt das Pagersteuerelement seine Schaltflächengröße auf drei Viertel der Breite der Bildlaufleiste fest.

Die Pagerschaltfläche hat eine Mindestgröße von derzeit 12 Pixeln. Dies kann sich jedoch ändern, sodass Sie sich nicht auf diesen Wert verlassen sollten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PGM \_ GETBUTTONSIZE**](pgm-getbuttonsize.md)
</dt> </dl>

 

 





