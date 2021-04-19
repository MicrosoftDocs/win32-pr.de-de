---
title: Finger einfügeinjektion
description: Dieser Abschnitt enthält die Referenz Spezifikationen für Finger einschleusungs Konstanten.
ms.assetid: 52941DF1-88AF-452B-BF3E-838ADBDBC9B2
topic_type:
- apiref
api_name:
- MAX_TOUCH_COUNT
- TOUCH_FEEDBACK_DEFAULT
- TOUCH_FEEDBACK_INDIRECT
- TOUCH_FEEDBACK_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 76a763a7153bbb9aa67254ffeb5e994a55426e43
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106372536"
---
# <a name="touch-injection-constants"></a>Finger einfügeinjektion

Dieser Abschnitt enthält die Referenz Spezifikationen für Finger [einschleusungs](touch-injection-portal.md) Konstanten.

| Konstante/Wert | BESCHREIBUNG |
|---|---|
| **MAX_TOUCH_COUNT** 256                            | Gibt die maximale Anzahl von gleichzeitigen Kontakten an.<br/> |
| **TOUCH_FEEDBACK_DEFAULT** 0x1    | Gibt Standard-Fingereingabe Visualisierungen an.<br/>                |
| **TOUCH_FEEDBACK_INDIRECT** 0x2 | Gibt indirekte Berührungs Visualisierungen an.<br/>               |
| **TOUCH_FEEDBACK_NONE** 0x3             | Gibt keine Berührungs Visualisierungen an.<br/>                     |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Nur Windows 8 \[ -Desktop-Apps\]                                           |
| Unterstützte Mindestversion (Server) | Nur Windows Server 2012 \[ -Desktop-Apps\]                                 |
| Header                   | Winuser. h |

## <a name="see-also"></a>Siehe auch

[Touchscreen-Referenz](touch-injection-reference.md)
