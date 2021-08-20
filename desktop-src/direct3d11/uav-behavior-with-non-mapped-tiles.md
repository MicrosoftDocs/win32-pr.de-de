---
title: UAV-verhalten bei nicht zugeordneten Kacheln
description: Das Verhalten von Unordered Access View (UAV) Lese- und Schreibvorgängen hängt vom Grad der Hardwareunterstützung ab.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed676403e5eb1fdc838ac080b8be530b5004e6734fedc5674664f4d75304ee37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857660"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a>UAV-verhalten bei nicht zugeordneten Kacheln

Das Verhalten von Unordered Access View (UAV) Lese- und Schreibvorgängen hängt vom Grad der Hardwareunterstützung ab. Eine Aufschlüsselung der Anforderungen finden Sie unter Allgemeines Lese- und Schreibverhalten für [die Featuresebenen für gekachelte Ressourcen.](tiled-resources-features-tiers.md) In diesem Abschnitt wird das ideale Verhalten zusammengefasst.

Shadervorgänge, die aus einer nicht zugeordneten Kachel in einem UAV lesen, geben 0 in allen nicht fehlenden Komponenten des Formats und den Standardwert für fehlende Komponenten zurück.

Shadervorgänge, die versuchen, in eine nicht zugeordnete Kachel zu schreiben, bewirken, dass nichts in den nicht zugeordneten Bereich geschrieben wird (während Schreibvorgänge in einen zugeordneten Bereich fortgesetzt werden). Diese ideale Definition für die Schreibverarbeitung ist für [Ebene 2](tier-2.md)nicht erforderlich. Schreibvorgänge in nicht zugeordnete Kacheln können in einem Cache enden, den nachfolgende Lesevorgänge aufnehmen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pipelinezugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




