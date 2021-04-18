---
title: Positions Attribut (H) (VML)
description: Positions Attribut (H) (VML)
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340936"
---
# <a name="position-attribute-hvml"></a>Positions Attribut (H) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt THEX-und y-Werte des Handles an. Lese-/Schreib-VgVector2D. 

**Gilt für**

[H](msdn-online-vml-h-element.md) (Unterelement von [Handles](msdn-online-vml-handles-element.md))

**Tagsyntax**

<v: *Element* Position = " *Ausdruck* " >

**Anmerkungen**

x-und y-Werte können einen der folgenden Typen aufweisen:

-   Konstante
-   Formel (z. b. @2 )
-   anpassen (z. b. \# 3)
-   Zentrum
-   TopLeft
-   BottomRight

Wenn einer der obigen Typen außer " *Anpassen* " angegeben ist, wird die Position des Handles in dieser Dimension korrigiert. Wenn ein Anpassungs handle angegeben ist, kann das Handle in dieser Dimension verschoben werden, und der Anpassungswert wird durch die Position des Handles bestimmt.

Wenn ein [Polar](msdn-online-vml-polar-attribute.md) Attribut angegeben wird, stellt das **Positions** Attribut die RADIUS-und Winkelwerte des Handles anstelle von x und y dar.

Der Standardwert ist 0,0.

*VML-Standard Attribut*

 

 