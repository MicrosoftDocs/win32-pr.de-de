---
description: Das swapinputs-Attribut gibt an, ob Übergangseingaben ausgetauscht werden sollen. Wenn der Wert TRUE ist, werden die Eingaben ausgetauscht. Der Standardwert ist FALSE.
ms.assetid: 2b8d95ec-2c6c-4bd8-83e9-7f72770449b5
title: swapinputs-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b74d16d9b195f504188f4684cf234a5b0c7627274c6e74d57e6824df20a0c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951709"
---
# <a name="swapinputs-attribute"></a>swapinputs-Attribut

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Das `swapinputs` -Attribut gibt an, ob Übergangseingaben ausgetauscht werden sollen. Wenn der Wert **TRUE** ist, werden die Eingaben ausgetauscht. Der Standardwert ist **FALSE**.

## <a name="possible-values"></a>Mögliche Werte

Die folgenden Werte sind als TRUE definiert: y, Y, t, T, 1. Die folgenden Werte sind als FALSE definiert: n, N, f, F, 0 (null).

## <a name="applies-to"></a>Gilt für

[**Übergang**](transition-element.md)

## <a name="remarks"></a>Hinweise

Standardmäßig wird ein Übergang von der zusammengesetzten aller Ebenen mit niedrigerer Priorität zu der Ebene fortgesetzt, auf der sich der Übergang befindet. Wenn das `swapinputs` Attribut 1 ist, wird diese Richtung umgekehrt. Weitere Informationen zum vom DES verwendeten Ebenenmodell finden Sie unter [Das Zeitachsenmodell.](the-timeline-model.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md)
</dt> </dl>

 

 



