---
title: LB_SETHORIZONTALEXTENT Meldung (Winuser.h)
description: Legt die Breite in Pixel fest, mit der ein Listenfeld horizontal gescrollt werden kann (die bildlauffähige Breite).
ms.assetid: 7d59b6de-2a22-4246-936b-4c669d285392
keywords:
- LB_SETHORIZONTALEXTENT Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: ce248354b853dd3be15e76646958ed25068648182970d748da35fb5c596ca49e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433879"
---
# <a name="lb_sethorizontalextent-message"></a>LB \_ SETHORIZONTALEXTENT-Nachricht

Legt die Breite in Pixel fest, mit der ein Listenfeld horizontal gescrollt werden kann (die bildlauffähige Breite). Wenn die Breite des Listenfelds kleiner als dieser Wert ist, führt die horizontale Scrollleiste einen horizontalen Bildlauf für Elemente im Listenfeld aus. Wenn die Breite des Listenfelds gleich oder größer als dieser Wert ist, wird die horizontale Bildlaufleiste ausgeblendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die Anzahl der Pixel an, um die das Listenfeld gescrollt werden kann.

Windows 95/Windows 98/Windows Edition (Windows Me): Der *wParam-Parameter* ist auf 16-Bit-Werte beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Um auf die **LB \_ SETHORIZONTALEXTENT-Nachricht** zu reagieren, muss das Listenfeld mit dem [**WS \_ HSCROLL-Stil**](/windows/desktop/winmsg/window-styles) definiert worden sein.

Beachten Sie, dass ein Listenfeld seinen horizontalen Umfang nicht dynamisch aktualisiert.

Diese Meldung hat keine Auswirkungen auf ein Listenfeld mit mehreren Spalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LB \_ GETHORIZONTALEXTENT**](lb-gethorizontalextent.md)
</dt> </dl>

 

