---
title: Portieren von Kurven- und Oberflächenfunktionen
description: Portieren von Kurven- und Oberflächenfunktionen
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- IRIS GL-Portierung, Kurven
- Portieren von IRIS GL,Kurven
- Portieren von IRIS GL,Curves zu OpenGL
- OpenGL-Portierung von IRIS GL,Curves
- IRIS GL-Portierung, Oberflächenpatches
- Portieren von IRIS GL,Oberflächenpatches
- Portieren von IRIS GL zu OpenGL, Oberflächenpatches
- OpenGL-Portierung von IRIS GL, Oberflächenpatches
- Kurven
- Oberflächenpatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed76109bb0067996c26acf48bff7a58773220ad1eb87e13d617bddedeb6d62a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777040"
---
# <a name="porting-curve-and-surface-functions"></a>Portieren von Kurven- und Oberflächenfunktionen

OpenGL unterstützt keine Entsprechungen zu den IRIS GL-Funktionen für Kurven und Oberflächenpatches. Sie müssen Ihren Code neu schreiben, wenn er einen der folgenden Aufrufe enthält:

-   **defbasis**
-   **curvebasis,** **curveprecision,** **crv,** **crvn,** **rcrv,** **rcrvn** und **curveit**
-   **patchbasis,** **patchcurves,** **patchprecision,** **patch** und **rpatch**

Dieses Thema enthält Informationen zu folgenden Themen.

-   [Portieren von NURBS-Objekten](porting-nurbs-objects.md)
-   [Portieren von NURBS-Kurven](porting-nurbs-curves.md)
-   [Portieren von Kürzungskurven](porting-trimming-curves.md)
-   [Portieren von NURBS-Oberflächen](porting-nurbs-surfaces.md)

 

 




