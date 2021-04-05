---
title: LB_SETHORIZONTALEXTENT Meldung (Winuser. h)
description: Legt die Breite (in Pixel) fest, um die ein Listenfeld Horizontal (die scrollbare Breite) gescrollt werden kann.
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- Windows-Steuerelemente für LB_SETHORIZONTALEXTENT Meldung
topic_type:
- apiref
api_name:
- LB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded17b9ea2d78a77b030950877047256d0e2a1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859163"
---
# <a name="lb_sethorizontalextent-message"></a>LB- \_ Nachricht

Legt die Breite (in Pixel) fest, um die ein Listenfeld Horizontal (die scrollbare Breite) gescrollt werden kann. Wenn die Breite des Listen Felds kleiner als dieser Wert ist, führt die horizontale Schiebe Leiste einen horizontalen Bildlauf durch Elemente im Listenfeld aus. Wenn die Breite des Listen Felds größer oder gleich diesem Wert ist, wird die horizontale Schiebe Leiste ausgeblendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die Anzahl der Pixel an, um die das Listenfeld gescrollt werden kann.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Um auf die **lb- \_ lthorizontalblock** -Nachricht zu reagieren, muss das Listenfeld mit dem [**WS- \_ HScroll**](/windows/desktop/winmsg/window-styles) -Stil definiert worden sein.

Beachten Sie, dass ein Listenfeld seinen horizontalen Block nicht dynamisch aktualisiert.

Diese Meldung hat keine Auswirkung auf ein Listenfeld mit mehreren Spalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LB- \_ gethorizontalblock**](lb-gethorizontalextent.md)
</dt> </dl>

 

