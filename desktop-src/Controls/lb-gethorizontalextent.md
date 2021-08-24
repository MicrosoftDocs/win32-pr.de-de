---
title: LB_GETHORIZONTALEXTENT Meldung (Winuser.h)
description: Ruft die Breite in Pixel ab, die ein Listenfeld horizontal scrollen kann (die scrollbare Breite), wenn das Listenfeld über eine horizontale Scrollleiste verfügt.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- LB_GETHORIZONTALEXTENT Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 01f754b62ad0f51a236662fdfba2304221d58e1288e2756c0330343c63a0699e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799510"
---
# <a name="lb_gethorizontalextent-message"></a>LB \_ GETHORIZONTALEXTENT-Nachricht

Ruft die Breite in Pixel ab, die ein Listenfeld horizontal scrollen kann (die scrollbare Breite), wenn das Listenfeld über eine horizontale Scrollleiste verfügt.

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

Der Rückgabewert ist die bildlauffähige Breite des Listenfelds in Pixel.

## <a name="remarks"></a>Hinweise

Um auf die **LB \_ GETHORIZONTALEXTENT-Nachricht** zu reagieren, muss das Listenfeld mit dem [**WS \_ HSCROLL-Stil**](/windows/desktop/winmsg/window-styles) definiert worden sein.

Wenn die Anwendung den horizontalen Umfang des Listenfelds nicht festgelegt (mit [**LB \_ SETHORIZONTALEXTENT),**](lb-sethorizontalextent.md)ist der horizontale Standardumfang 0 (null). Beachten Sie, dass der horizontale Umfang des Listenfelds nicht dynamisch aktualisiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> </dl>

 

