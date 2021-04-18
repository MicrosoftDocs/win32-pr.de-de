---
title: Verhalten der Berührungs Treffer Tests
description: Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu identifizieren, wie Nachrichten für touchtreffer Tests von Fenstern verarbeitet werden, die über die registertouchhittestingwindow-Funktion registriert werden.
ms.assetid: D1ECCBFA-CD01-401E-A42E-4F954F5F0A32
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
ms.date: 02/07/2020
ms.openlocfilehash: 9b49f61870c6c7041d73d6fa8d5c078887360359
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345497"
---
# <a name="touch-hit-testing-behaviors"></a>Verhalten der Berührungs Treffer Tests

Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu identifizieren, wie Nachrichten für touchtreffer Tests von Fenstern verarbeitet werden, die über die [**registertouchhittestingwindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) -Funktion registriert werden.

| Konstante/Wert | BESCHREIBUNG |
|---|---|
| **TOUCH_HIT_TESTING_DEFAULT** </dt> <dt>0 (0x0) | Gibt an, dass [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) -Nachrichten nicht an das Zielfenster gesendet, sondern an untergeordnete Fenster gesendet werden.<br/> |
| **TOUCH_HIT_TESTING_CLIENT** </dt> <dt>1 (0x1)    | Gibt an, dass [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) -Nachrichten an das Zielfenster gesendet werden.<br/>                                   |
| **TOUCH_HIT_TESTING_NONE** </dt> <dt>2 (0x2)          | Gibt an, dass [WM_TOUCHHITTESTING](../inputmsg/wm-touchhittesting.md) -Nachrichten nicht an das Zielfenster oder die untergeordneten Fenster gesendet werden.<br/>              |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | <dl> <dt>Winuser. h |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konstanten](constants.md)
