---
title: UAV-verhalten bei nicht zugeordneten Kacheln
description: Das Verhalten von Lese-und Schreibvorgängen für die ungeordnete Zugriffs Ansicht (UAV) hängt von der Hardwareunterstützung ab.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9909f8faecd3345761ae26e60835c77aae9ab3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947469"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a>UAV-verhalten bei nicht zugeordneten Kacheln

Das Verhalten von Lese-und Schreibvorgängen für die ungeordnete Zugriffs Ansicht (UAV) hängt von der Hardwareunterstützung ab. Eine Aufschlüsselung der Anforderungen finden Sie unter Allgemeines Lese-und Schreibverhalten für die [Features der gekachelten Ressourcen](tiled-resources-features-tiers.md). In diesem Abschnitt wird das ideale Verhalten zusammengefasst.

Shadervorgänge, die von einer nicht zugeordneten Kachel in einer UAV lesen, geben 0 (null) in allen nicht fehlenden Komponenten des Formats und die Standardeinstellung für fehlende Komponenten zurück.

Shadervorgänge, die versuchen, in eine nicht zugeordnete Kachel zu schreiben, bewirken, dass nichts in den nicht zugeordneten Bereich geschrieben wird (während Schreibvorgänge in einen zugeordneten Bereich fortgesetzt werden). Diese ideale Definition für die Schreib Behandlung ist für [Ebene 2](tier-2.md)nicht erforderlich. Schreibvorgänge in nicht zugeordnete Kacheln können in einem Cache landen, den nachfolgende Lesevorgänge aufnehmen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pipeline Zugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




