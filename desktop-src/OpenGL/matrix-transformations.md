---
title: Matrix Transformationen
description: Vertices und normale werden von Modelview und Projektions Matrizen transformiert, bevor Sie zum Entwickeln eines Bilds im Framebuffer verwendet werden.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- OpenGL-Verarbeitungs Pipeline, Matrizen
- Matrizen OpenGL
- Modelview-Matrix
- Projektions Matrix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db0ebd8bd13b8d2cee32b8873f697ab073140bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206659"
---
# <a name="matrix-transformations"></a><span data-ttu-id="0592a-107">Matrix Transformationen</span><span class="sxs-lookup"><span data-stu-id="0592a-107">Matrix Transformations</span></span>

<span data-ttu-id="0592a-108">Vertices und normale werden von Modelview und Projektions Matrizen transformiert, bevor Sie zum Entwickeln eines Bilds im Framebuffer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0592a-108">Vertices and normals are transformed by the modelview and projection matrices before they're used to produce an image in the framebuffer.</span></span> <span data-ttu-id="0592a-109">Verwenden Sie Funktionen wie z. b. [**glMatrixMode**](glmatrixmode.md) [**, \* glmultmatrix**](glmultmatrix.md), [**glrotation \***](glrotate.md), [**gltranslate \***](gltranslate.md)und [**glscale \***](glscale.md) , um die gewünschten Transformationen zu verfassen.</span><span class="sxs-lookup"><span data-stu-id="0592a-109">Use functions such as [**glMatrixMode**](glmatrixmode.md), [**glMultMatrix\***](glmultmatrix.md), [**glRotate\***](glrotate.md), [**glTranslate\***](gltranslate.md), and [**glScale\***](glscale.md) to compose the desired transformations.</span></span> <span data-ttu-id="0592a-110">Oder Sie geben Matrizen direkt mit " [**glloadmatrix \***](glloadmatrix.md) " und " [**glLoadIdentity**](glloadidentity.md)" an.</span><span class="sxs-lookup"><span data-stu-id="0592a-110">Or specify matrices directly with [**glLoadMatrix\***](glloadmatrix.md) and [**glLoadIdentity**](glloadidentity.md).</span></span> <span data-ttu-id="0592a-111">Verwenden Sie [**glPushMatrix**](glpushmatrix.md) und [**glPopMatrix**](glpopmatrix.md) , um Modelview-und Projektions Matrizen auf ihren jeweiligen Stapeln zu speichern und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="0592a-111">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore modelview and projection matrices on their respective stacks.</span></span>

 

 




