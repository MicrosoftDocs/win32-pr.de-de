---
title: Rasterizerverhalten bei nicht zugeordneten Kacheln
description: In diesem Abschnitt wird das Verhalten des Rasterizers mit nicht zugeordneten Kacheln beschrieben.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992814"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a>Rasterizerverhalten bei nicht zugeordneten Kacheln

In diesem Abschnitt wird das Verhalten des Rasterizers mit nicht zugeordneten Kacheln beschrieben.

## <a name="depthstencilview"></a>Depthstencilview

Das Verhalten von Lese-und Schreibvorgängen in der tiefen Schablone ist abhängig von der Hardwareunterstützung. Eine Aufschlüsselung der Anforderungen finden Sie unter Allgemeines Lese-und Schreibverhalten für die [Features der gekachelten Ressourcen](tiled-resources-features-tiers.md).

Hier ist das ideale Verhalten:

Wenn eine Kachel nicht in der depthstencilview zugeordnet ist, ist der Rückgabewert aus der Lesetiefe 0 (null), der dann in alle Vorgänge eingefügt wird, die für den Wert der tiefen Lesevorgänge konfiguriert sind. Schreibvorgänge in die Kachel "fehlende tiefe" werden gelöscht. Diese ideale Definition für die Schreib Behandlung ist für [Ebene 2](tier-2.md)nicht erforderlich. Schreibvorgänge in nicht zugeordnete Kacheln können in einem Cache landen, den nachfolgende Lesevorgänge aufnehmen können.

## <a name="rendertargetview"></a>Rendertargetview

Das Verhalten von Lese-und Schreibvorgängen der renderzielansicht (RTV) hängt von der Hardwareunterstützung ab. Eine Aufschlüsselung der Anforderungen finden Sie unter Allgemeines Lese-und Schreibverhalten für die [Features der gekachelten Ressourcen](tiled-resources-features-tiers.md).

Bei allen Implementierungen können unterschiedliche, gleichzeitig gebundene rtvs (und DSV) verschiedene Bereiche zugeordnet werden, die nicht zugeordnet sind und unterschiedliche Größen Oberflächen Formate aufweisen können (Dies bedeutet verschiedene Kachel Formen).

Hier ist das ideale Verhalten:

Lesevorgänge aus rtvs geben 0 in fehlenden Kacheln zurück, und Schreibvorgänge werden gelöscht. Diese ideale Definition für die Schreib Behandlung ist für [Ebene 2](tier-2.md)nicht erforderlich. Schreibvorgänge in nicht zugeordnete Kacheln können in einem Cache landen, den nachfolgende Lesevorgänge aufnehmen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pipeline Zugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




