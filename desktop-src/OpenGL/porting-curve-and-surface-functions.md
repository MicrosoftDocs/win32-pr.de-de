---
title: Portieren von Kurven-und Oberflächen Funktionen
description: Portieren von Kurven-und Oberflächen Funktionen
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- IRIS GL portieren, Kurven
- Portieren von IRIS GL, Kurven
- Portieren auf OpenGL von IRIS GL, Kurven
- OpenGL-Portierung von IRIS GL, Kurven
- IRIS GL portieren, Surface-Patches
- Portieren von IRIS GL, Surface-Patches
- Portieren auf OpenGL von IRIS GL, Surface-Patches
- OpenGL-Portierung von IRIS GL, Surface-Patches
- Kurven
- Surface-Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3caedc89697d1c83325a00b3dc1cb55c34612e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309455"
---
# <a name="porting-curve-and-surface-functions"></a>Portieren von Kurven-und Oberflächen Funktionen

OpenGL unterstützt keine Entsprechungen der Iris GL-Funktionen für Kurven und Oberflächen Patches. Sie müssen Ihren Code neu schreiben, wenn er einen der folgenden Aufrufe umfasst:

-   **mit defbasis**
-   **"Cursor**", " **Cursor Genauigkeit**", " **CRV**", " **crvN**", " **rcrv**", " **rcrvn**" und " **Cursor** "
-   **Patchbasis**, **patchkurven**, **patchgenauigkeit**, **Patch** und **rpatch**

Dieses Thema enthält Informationen zu den folgenden Themen.

-   [Portieren von nursb-Objekten](porting-nurbs-objects.md)
-   [Portieren von nursb-Kurven](porting-nurbs-curves.md)
-   [Portieren von Kürzungs Kurven](porting-trimming-curves.md)
-   [Portieren von nursb-Oberflächen](porting-nurbs-surfaces.md)

 

 




