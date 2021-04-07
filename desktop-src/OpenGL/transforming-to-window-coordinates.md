---
title: Transformieren in Fenster Koordinaten
description: Bevor Clip Koordinaten in Fenster Koordinaten konvertiert werden, werden Sie durch den Wert von w dividiert, um normalisierte Geräte Koordinaten zu erzielen.
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- OpenGL-Verarbeitungs Pipeline, Konvertierungen in Fenster Koordinaten
- Wechseln in Fenster Koordinaten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ec3d8922890cfa3a79c5dacd94e93a06c53a73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713925"
---
# <a name="transforming-to-window-coordinates"></a><span data-ttu-id="7b570-105">Transformieren in Fenster Koordinaten</span><span class="sxs-lookup"><span data-stu-id="7b570-105">Transforming to Window Coordinates</span></span>

<span data-ttu-id="7b570-106">Bevor Clip Koordinaten in Fenster Koordinaten konvertiert werden, werden Sie durch den Wert von *w* dividiert, um normalisierte Geräte Koordinaten zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="7b570-106">Before clip coordinates are converted to window coordinates, they are divided by the value of *w* to yield normalized device coordinates.</span></span> <span data-ttu-id="7b570-107">Die auf diese normalisierte Koordinaten angewendete viewporttransformation erzeugt Fenster Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="7b570-107">The viewport transformation applied to these normalized coordinates produces window coordinates.</span></span> <span data-ttu-id="7b570-108">Sie steuern den Viewport, der den Bereich des Bildschirm Fensters bestimmt, in dem ein Bild mit " [**gldepthrange**](gldepthrange.md) " und " [**glViewport**](glviewport.md)" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7b570-108">You control the viewport, which determines the area of the on-screen window that displays an image, with [**glDepthRange**](gldepthrange.md) and [**glViewport**](glviewport.md).</span></span>

 

 




