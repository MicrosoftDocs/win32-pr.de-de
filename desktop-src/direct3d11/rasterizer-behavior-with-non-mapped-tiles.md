---
title: Rasterizerverhalten bei nicht zugeordneten Kacheln
description: In diesem Abschnitt wird das Verhalten des Rasterizers mit nicht zugeordneten Kacheln beschrieben.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16612e8538ec57178ed053ae1a6333c11fcaa6e4454b387408f3d99c6004eb47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608510"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a>Rasterizerverhalten bei nicht zugeordneten Kacheln

In diesem Abschnitt wird das Verhalten des Rasterizers mit nicht zugeordneten Kacheln beschrieben.

## <a name="depthstencilview"></a>DepthStencilView

Das Verhalten von Lese- und Schreibvorgängen in der Tiefenschablonenansicht (Depth Stencil View, DSV) hängt vom Grad der Hardwareunterstützung ab. Eine Aufschlüsselung der Anforderungen finden Sie unter Allgemeines Lese- und Schreibverhalten für [die Featuresebenen für gekachelte Ressourcen.](tiled-resources-features-tiers.md)

Hier ist das ideale Verhalten:

Wenn eine Kachel nicht in DepthStencilView zugeordnet ist, ist der Rückgabewert aus der Lesetiefe 0, der dann in alle Vorgänge eingespeist wird, die für den Tiefenlesewert konfiguriert sind. Schreibvorgänge in die fehlende Tiefenkachel werden gelöscht. Diese ideale Definition für die Schreibverarbeitung ist für [Ebene 2](tier-2.md)nicht erforderlich. Schreibvorgänge in nicht zugeordnete Kacheln können in einem Cache enden, den nachfolgende Lesevorgänge aufnehmen können.

## <a name="rendertargetview"></a>RenderTargetView

Das Verhalten von Lese- und Schreibvorgängen in der Renderzielansicht hängt vom Grad der Hardwareunterstützung ab. Eine Aufschlüsselung der Anforderungen finden Sie unter Allgemeines Lese- und Schreibverhalten für [die Featuresebenen für gekachelte Ressourcen.](tiled-resources-features-tiers.md)

Bei allen Implementierungen können verschiedene RTVs (und DSV), die gleichzeitig gebunden sind, unterschiedliche Bereiche im Vergleich zu nicht zugeordneten Bereichen aufweisen und unterschiedliche Oberflächenformate unterschiedlicher Größe aufweisen (d. h. unterschiedliche Kachelformen).

Hier ist das ideale Verhalten:

Lesevorgänge von RTVs geben 0 in fehlenden Kacheln zurück, und Schreibvorgänge werden gelöscht. Diese ideale Definition für die Schreibverarbeitung ist für [Ebene 2](tier-2.md)nicht erforderlich. Schreibvorgänge in nicht zugeordnete Kacheln können in einem Cache enden, den nachfolgende Lesevorgänge aufnehmen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pipelinezugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




