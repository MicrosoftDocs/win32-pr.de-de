---
title: Touch-Treffertestergebnisse
description: Die folgenden Konstanten identifizieren die möglichen Treffertestergebnisse für ein Objekt relativ zu anderen Objekten, die den Berührungskontaktbereich überschneiden.
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 18b321272637f4e6931bdc9115e64f8b0553e90e94d8013147ca7a577bad1eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758012"
---
# <a name="touch-hit-testing-scores"></a>Touch-Treffertestergebnisse

Die folgenden Konstanten identifizieren die möglichen Treffertestergebnisse für ein Objekt relativ zu anderen Objekten, die den Berührungskontaktbereich überschneiden.

| Konstante/Wert | BESCHREIBUNG |
|---|---|
| **TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0      | Das -Objekt ist das wahrscheinlichste Ziel.<br/>  |
| **TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF | Das -Objekt ist das am wenigsten wahrscheinliche Ziel.<br/> |

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                            |
| Header<br/>                   | Winuser.h |
