---
title: LB_GETHORIZONTALEXTENT Meldung (Winuser. h)
description: Ruft die Breite in Pixel ab, in der ein Listenfeld Horizontal (die scrollbare Breite) gescrollt werden kann, wenn das Listenfeld eine horizontale Schiebe Leiste hat.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- Windows-Steuerelemente für LB_GETHORIZONTALEXTENT Meldung
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf10f4f216e0c00fba256c1373fb9aae4f2a4ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957106"
---
# <a name="lb_gethorizontalextent-message"></a>LB- \_ gethorizontalblock-Nachricht

Ruft die Breite in Pixel ab, in der ein Listenfeld Horizontal (die scrollbare Breite) gescrollt werden kann, wenn das Listenfeld eine horizontale Schiebe Leiste hat.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die scrollbare Breite des Listen Felds in Pixel.

## <a name="remarks"></a>Bemerkungen

Um auf die **lb- \_ gethorizontalblock** -Nachricht zu reagieren, muss das Listenfeld mit dem [**WS- \_ HScroll**](/windows/desktop/winmsg/window-styles) -Stil definiert worden sein.

Wenn die Anwendung den horizontalen Wertebereich des Listen Felds (mit [**lb- \_ sethorizontalblock**](lb-sethorizontalextent.md)) nicht festgelegt hat, ist der standardmäßige horizontale Block NULL. Beachten Sie, dass das Listenfeld den horizontalen Block nicht dynamisch aktualisiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB-Abbild \_ Umfang**](lb-sethorizontalextent.md)
</dt> </dl>

 

