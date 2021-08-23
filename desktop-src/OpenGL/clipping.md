---
title: Clipping (OpenGL)
description: Clipping erfolgt in zwei Schritten
ms.assetid: f6f60135-f43b-4595-bfd3-33e750413e70
keywords:
- OpenGL-Verarbeitungspipeline, Clipping
- Beschneiden von OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb518b9208b73dad2071531f6a30cdff6cab2ec5dcbe937fa3e66fea8bb0a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289040"
---
# <a name="clipping-opengl"></a>Clipping (OpenGL)

Clipping erfolgt in zwei Schritten:

1.  **Anzeigen von VolumeclippingApplication-specific clipping (Volumeclipping)Application-specific clipping (Volumeclipping anzeigen)Application-specific clipping (** Unmittelbar nach dem Zusammensetzen von Primitiven werden sie bei Bedarf in Augenkoordinaten für alle Clippingebenen abgeschnitten, die Sie mit [**glClipPlane**](glclipplane.md)definiert haben. (OpenGL erfordert Unterstützung für mindestens sechs solche anwendungsspezifischen Clippingebenen.)
2.  Primitive werden von der Projektionsmatrix in Clipkoordinaten transformiert und vom entsprechenden Ansichtsvolumen abgeschnitten. Diese Matrix kann durch die Matrixtransformationsfunktionen gesteuert werden (siehe [Matrixtransformationen),](matrix-transformations.md)wird jedoch in der Regel durch [**glFrustum**](glfrustum.md) oder [**glOrtho**](glortho.md)angegeben.

Punkte, Liniensegmente und Polygone werden während des Clippings unterschiedlich behandelt:

-   Punkte werden entweder im ursprünglichen Zustand beibehalten (wenn sie sich innerhalb des Clipvolumes befinden) oder verworfen (wenn sie sich außerhalb des Clipvolumes befinden).
-   Wenn sich Teile von Liniensegmenten oder Polygonen außerhalb des Clipvolumens befinden, werden neue Scheitelpunkte an den Clippunkten generiert.
-   Bei Polygonen muss möglicherweise ein ganzer Rand zwischen neuen Scheitelpunkten erstellt werden, die an den Clippunkten generiert werden.
-   Für Liniensegmente und Polygone, die abgeschnitten werden, werden das Randflag, die Farbe und die Texturinformationen allen neuen Scheitelpunkten zugewiesen.

 

 




