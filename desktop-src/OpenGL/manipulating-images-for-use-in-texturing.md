---
title: Bearbeiten von Bildern für die Verwendung in der Texturierung
description: Die OpenGL Utility Library (GLU) bietet Bildskalierung und automatische Mipmapping-Funktionen, um die Spezifikation von Textur Bildern zu vereinfachen.
ms.assetid: 20edf665-1fed-4761-b8b1-beee02c78b0d
keywords:
- OpenGL-Hilfsprogramm (GLU), Bildskalierung
- GLU (OpenGL-Hilfsprogramm), Bildskalierung
- OpenGL-Hilfsprogramm (GLU), automatisches Mipmapping
- GLU (OpenGL-Hilfsprogramm), automatische Mipmapping
- OpenGL-Hilfsprogramm (GLU), Textur Bilder
- GLU (OpenGL-Hilfsprogramm), Textur Bilder
- Glu-Bibliothek, Textur Bilder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16726493bbcb6e0116e4c158e470029f34f5b652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309795"
---
# <a name="manipulating-images-for-use-in-texturing"></a><span data-ttu-id="4f01b-110">Bearbeiten von Bildern für die Verwendung in der Texturierung</span><span class="sxs-lookup"><span data-stu-id="4f01b-110">Manipulating Images for Use in Texturing</span></span>

<span data-ttu-id="4f01b-111">Die OpenGL Utility Library (GLU) bietet Bildskalierung und automatische Mipmapping-Funktionen, um die Spezifikation von Textur Bildern zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="4f01b-111">The OpenGL Utility library (GLU) provides image scaling and automatic mipmapping functions to simplify the specification of texture images.</span></span> <span data-ttu-id="4f01b-112">Die Funktion " [**gluscaleimage**](gluscaleimage.md) " skaliert ein angegebenes Bild auf eine akzeptierte Textur Größe. Sie können das resultierende Bild als Textur an OpenGL übergeben.</span><span class="sxs-lookup"><span data-stu-id="4f01b-112">The [**gluScaleImage**](gluscaleimage.md) function scales a specified image to an accepted texture size; you can pass the resulting image to OpenGL as a texture.</span></span> <span data-ttu-id="4f01b-113">Die automatischen Mipmapping-Funktionen, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) und [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), erstellen mipzugeordnete Textur Bilder aus einem angegebenen Bild und übergeben Sie an [**glTexImage1D**](glteximage1d.md) bzw. [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="4f01b-113">The automatic mipmapping functions, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) and [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), create mipmapped texture images from a specified image and pass them to [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md), respectively.</span></span>

 

 




