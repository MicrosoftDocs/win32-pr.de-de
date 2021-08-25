---
title: Konstanten im Touch-Treffertestfenster
description: Gibt an, wie Nachrichten für Touchtreffertests von Fenstern verarbeitet werden, die über die RegisterTouchHitTestingWindow-Funktion registriert werden.
ms.assetid: CC6CCD0B-882F-4DA7-B886-D4BD18D6060C
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ccc26947241d5d777cacee504a066b7e070faf0a8febc39b86571537c14245f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829750"
---
# <a name="touch-hit-testing-window-constants"></a>Konstanten im Touch-Treffertestfenster

Gibt an, wie Nachrichten für Touchtreffertests von Fenstern verarbeitet werden, die über die [**RegisterTouchHitTestingWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) registriert werden.



| Konstante/Wert                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TOUCH_HIT_TESTING_DEFAULT"></span><span id="touch_hit_testing_default"></span><dl> <dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt> </dl> | [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) Nachrichten werden nicht an das Zielfenster, sondern an untergeordnete Fenster gesendet.<br/> |
| <span id="TOUCH_HIT_TESTING_CLIENT"></span><span id="touch_hit_testing_client"></span><dl> <dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt> </dl>    | [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) Nachrichten werden an das Zielfenster gesendet.<br/>                                   |
| <span id="TOUCH_HIT_TESTING_NONE"></span><span id="touch_hit_testing_none"></span><dl> <dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt> </dl>          | [**WM_TOUCHHITTESTING**](wm-touchhittesting.md) Nachrichten werden nicht an das Zielfenster oder untergeordnete Fenster gesendet.<br/>              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konstanten](constants.md)
</dt> <dt>

[**POINTER_INFO**](/previous-versions/windows/desktop/api)
</dt> </dl>

 

