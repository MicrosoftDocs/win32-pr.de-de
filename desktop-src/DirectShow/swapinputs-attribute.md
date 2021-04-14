---
description: Das swapinputs-Attribut gibt an, ob Übergangs Eingaben ausgetauscht werden sollen. Wenn der Wert true ist, werden die Eingaben ausgetauscht. Der Standardwert ist FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: Attribut "Swap-Eingaben"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e2f02c642283e90b994bcd1bfa9e05076a7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349068"
---
# <a name="swapinputs-attribute"></a>Attribut "Swap-Eingaben"

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das- `swapinputs` Attribut gibt an, ob Übergangs Eingaben ausgetauscht werden sollen. Wenn der Wert **true** ist, werden die Eingaben ausgetauscht. Der Standardwert ist **FALSE**.

## <a name="possible-values"></a>Mögliche Werte

Die folgenden Werte sind als true definiert: y, y, t, t, 1. Die folgenden Werte sind als false definiert: n, n, f, f, 0 (null).

## <a name="applies-to"></a>Gilt für

[**Übergang**](transition-element.md)

## <a name="remarks"></a>Bemerkungen

Standardmäßig verläuft ein Übergang von der zusammengesetzten aller Ebenen mit niedrigerer Priorität zur Ebene, auf der sich der Übergang befindet. Wenn das- `swapinputs` Attribut 1 ist, wird diese Richtung umgekehrt. Weitere Informationen zum von des verwendeten Ebenenmodell finden Sie [im Zeitachsen Modell](the-timeline-model.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**Iamtimelinetrans::-wapinputs**](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



