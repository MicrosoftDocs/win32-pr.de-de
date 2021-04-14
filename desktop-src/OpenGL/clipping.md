---
title: Clipping (OpenGL)
description: Clipping erfolgt in zwei Schritten.
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- OpenGL-Verarbeitungs Pipeline, Clipping
- Clipping OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa35458e7e0a137759fe22be95f4b399b4d56b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391419"
---
# <a name="clipping-opengl"></a>Clipping (OpenGL)

Das Clipping erfolgt in zwei Schritten:

1.  **Anzeigen von Volume clippingapplication-Specific Clipping.** Unmittelbar nach dem Zusammenstellen von primitiven werden Sie bei Bedarf für alle clippingflächen, die Sie mit [**glclipplane**](glclipplane.md)definiert haben, in Augen Koordinaten abgeschnitten. (OpenGL erfordert Unterstützung für mindestens sechs anwendungsspezifische Clippingebenen.)
2.  Primitive werden von der Projektions Matrix in Clip Koordinaten transformiert und durch das entsprechende Ansichts Volume abgeschnitten. Diese Matrix kann von den Matrix Transformations Funktionen gesteuert werden (siehe [Matrix Transformationen](matrix-transformations.md)), wird jedoch in der Regel von [**glfrustum**](glfrustum.md) oder [**glortho**](glortho.md)angegeben.

Punkte, Liniensegmente und Polygone werden während des Clipping anders behandelt:

-   Punkte werden entweder in Ihrem ursprünglichen Zustand (wenn Sie sich im Ausschneide Volume befinden) aufbewahrt oder verworfen (wenn Sie sich außerhalb des Clip-Volumes befinden).
-   Wenn Teile von Liniensegmenten oder Polygone außerhalb des Clip Volumens liegen, werden an den Clip Punkten neue Scheitel Punkte generiert.
-   Bei Polygonen muss möglicherweise ein ganzer Rand zwischen neuen Scheitel Punkten erstellt werden, die an den Clip Punkten generiert werden.
-   Bei Liniensegmenten und Polygonen, die abgeschnitten werden, werden das Edge-Flag, die Farbe und die Textur Informationen allen neuen Scheitel Punkten zugewiesen.

 

 




