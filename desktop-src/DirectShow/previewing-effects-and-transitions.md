---
description: Vorschau von Effekten und Übergängen
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Vorschau von Effekten und Übergängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25506b7e50fe83c2e4fca7bb4166748ec43d33dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125078"
---
# <a name="previewing-effects-and-transitions"></a>Vorschau von Effekten und Übergängen

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Einige Effekte und Übergänge nehmen zum Rendervorgang relativ lange Zeit in Anspruch. Während der Vorschau kann dies dazu führen, dass das Video mit der Audiodatei nicht mehr synchron ist. Sie können die Vorschau Geschwindigkeit erhöhen, indem Sie Effekte oder Übergänge deaktivieren:

-   Um alle Effekte zu deaktivieren, nennen Sie [**iamtimeline:: enableeffects**](iamtimeline-enableeffects.md).
-   Um alle Übergänge zu deaktivieren, nennen Sie [**iamtimeline:: enabletransitions**](iamtimeline-enabletransitions.md).
-   Um einen bestimmten Übergang zu deaktivieren, nennen Sie [**iamtimelinetrans:: setcutsonly**](iamtimelinetrans-setcutsonly.md).

Wenn Effekte deaktiviert sind, werden Sie während der Vorschau nicht gerendert. Wenn ein Übergang deaktiviert ist, wird er als Sprung Ausschneide gerendert. Der segue zwischen den Spuren tritt immer noch auf, aber der visuelle Effekt wird nicht gerendert.

Wenn ein Effekt oder Übergang nicht gerendert werden kann, ersetzt die Renderengine einen Standardeffekt oder-Übergang. Aufrufen der [**iamtimeline:: setdefaulteffect**](iamtimeline-setdefaulteffect.md) -Methode zum Festlegen des Standard Effekts und der [**iamtimeline:: setdefaulttransition**](iamtimeline-setdefaulttransition.md) -Methode, um den Standard Übergang festzulegen. Wenn Sie keinen Standardwert angeben, oder wenn der von Ihnen angegebene Wert auch einen Fehler verursacht, verwendet des einen eigenen Standardwert.

> [!Note]  
> Sie können auch die Vorschau Qualität verbessern, indem Sie den Umfang der Rahmen Pufferung erhöhen. Weitere Informationen finden Sie unter [**iamtimelinegroup:: setoutputbuffering.**](iamtimelinegroup-setoutputbuffering.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



