---
description: Das Lock-Attribut gibt an, ob ein Objekt bearbeitet werden soll. Wenn der Wert TRUE ist, sollte die Anwendung das Objekt als gesperrt behandeln und Änderungen an diesem Objekt oder seinen unteren Objekten nicht zu lassen. Der Standardwert ist FALSE.
ms.assetid: 1aa92665-ab3b-4f04-9e6b-905942c197ef
title: lock-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdd1718c25aab136219af436543df064bd8f68bb53ea15b00e09e6a18188c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502320"
---
# <a name="lock-attribute"></a>lock-Attribut

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Das `lock` -Attribut gibt an, ob ein Objekt bearbeitet werden soll. Wenn der Wert **TRUE ist,** sollte die Anwendung das Objekt als gesperrt behandeln und Änderungen an diesem Objekt oder seinen unteren Objekten nicht zu lassen. Der Standardwert ist **FALSE**.

## <a name="possible-values"></a>Mögliche Werte

Mögliche Werte: Die folgenden Werte sind als TRUE definiert: y, Y, t, T, 1. Die folgenden Werte sind als FALSE definiert: n, N, f, F, 0 (null).

## <a name="applies-to"></a>Gilt für

[**clip**](clip-element.md), [**composite**](composite-element.md), [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetLocked**](iamtimelineobj-setlocked.md)
</dt> </dl>

 

 



