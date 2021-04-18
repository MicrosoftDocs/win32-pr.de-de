---
title: Texturkoordinaten werden erzeugt.
description: Anstatt die Texturkoordinaten explizit anzugeben, können Sie von OpenGL als Funktion anderer Scheitelpunkt Daten mithilfe von gltexgen \ generiert werden.
ms.assetid: 5c9ce163-6107-46a3-8c8d-fc87d2f8cf9a
keywords:
- OpenGL-Verarbeitungs Pipeline, Texturkoordinaten
- Texturkoordinaten OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d3f5b807f25aee2783ff8dab3a4930a9c797ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206982"
---
# <a name="generating-texture-coordinates"></a><span data-ttu-id="d7478-105">Texturkoordinaten werden erzeugt.</span><span class="sxs-lookup"><span data-stu-id="d7478-105">Generating Texture Coordinates</span></span>

<span data-ttu-id="d7478-106">Anstatt die Texturkoordinaten explizit anzugeben, können Sie von OpenGL als Funktion anderer Scheitelpunkt Daten mithilfe von [gltexgen \* ](gltexgen-functions.md)generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7478-106">Rather than explicitly supplying texture coordinates, you can have OpenGL generate them as a function of other vertex data using [glTexGen\*](gltexgen-functions.md).</span></span> <span data-ttu-id="d7478-107">Nachdem die Texturkoordinaten angegeben oder generiert wurden, werden Sie von der Textur Matrix transformiert.</span><span class="sxs-lookup"><span data-stu-id="d7478-107">After the texture coordinates have been specified or generated, they are transformed by the texture matrix.</span></span> <span data-ttu-id="d7478-108">Diese Matrix wird mit denselben Funktionen gesteuert, die für Matrix Transformationen verwendet werden (siehe [Matrix Transformationen](matrix-transformations.md)).</span><span class="sxs-lookup"><span data-stu-id="d7478-108">This matrix is controlled with the same functions that are used for matrix transformations (see [Matrix Transformations](matrix-transformations.md)).</span></span>

 

 




