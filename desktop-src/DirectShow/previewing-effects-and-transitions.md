---
description: Vorschau von Effekten und Übergängen
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Vorschau von Effekten und Übergängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8baa5f35511ca9b01990e1c3e0562a3a564204a52026c08e2e2827c154b166b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748300"
---
# <a name="previewing-effects-and-transitions"></a>Vorschau von Effekten und Übergängen

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Einige Effekte und Übergänge dauern relativ lange, bis sie gerendert werden. Während der Vorschau kann dies dazu führen, dass das Video gehackt oder nicht mehr mit dem Audio synchronisiert wird. Sie können die Vorschaugeschwindigkeit erhöhen, indem Sie Effekte oder Übergänge deaktivieren:

-   Um alle Effekte zu deaktivieren, rufen [**Sie IAMTimeline::EnableEffects auf.**](iamtimeline-enableeffects.md)
-   Um alle Übergänge zu deaktivieren, rufen [**Sie IAMTimeline::EnableTransitions auf.**](iamtimeline-enabletransitions.md)
-   Um einen bestimmten Übergang zu deaktivieren, rufen [**Sie IAMTimelineTrans::SetCutsOnly auf.**](iamtimelinetrans-setcutsonly.md)

Wenn Effekte deaktiviert sind, werden sie während der Vorschau nicht gerendert. Wenn ein Übergang deaktiviert ist, wird er als Sprungschnitt gerendert. Der Segue zwischen den Spuren tritt weiterhin auf, aber der visuelle Effekt wird nicht gerendert.

Wenn ein Effekt oder Übergang nicht gerendert werden kann, ersetzt die Render-Engine einen Standardeffekt oder -übergang. Rufen Sie [**die IAMTimeline::SetDefaultEffect-Methode**](iamtimeline-setdefaulteffect.md) auf, um den Standardeffekt und die [**IAMTimeline::SetDefaultTransition-Methode**](iamtimeline-setdefaulttransition.md) zum Festlegen des Standardübergangs fest. Wenn Sie keinen Standardwert angeben oder wenn die von Ihnen angegebenen ebenfalls einen Fehler verursachen, verwendet DES einen eigenen Standardwert.

> [!Note]  
> Sie können auch die Vorschauqualität verbessern, indem Sie die Framepufferung erhöhen. Siehe [**IAMTimelineGroup::SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



