---
description: Verwenden Sie zum Hinzufügen von Texturen die hierarchische Natur des Datei Formats, und fügen Sie den Material Datenobjekten ein optionales texturefilename-Datenobjekt hinzu.
ms.assetid: 741f4c05-49f8-4c76-be5c-ce5b496124bb
title: Hinzufügen von Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee0090b5990c2093a41efbd15eb998401ce2607
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126163"
---
# <a name="adding-textures-direct3d-9"></a><span data-ttu-id="c7f87-103">Hinzufügen von Texturen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c7f87-103">Adding Textures (Direct3D 9)</span></span>

<span data-ttu-id="c7f87-104">Verwenden Sie zum Hinzufügen von Texturen die hierarchische Natur des Datei Formats, und fügen Sie den [**Material**](material.md) Datenobjekten ein optionales [**texturefilename**](texturefilename.md) -Datenobjekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="c7f87-104">To add textures, use the hierarchical nature of the file format and add an optional [**TextureFilename**](texturefilename.md) data object to the [**Material**](material.md) data objects.</span></span> <span data-ttu-id="c7f87-105">Die **Material** -Objekte lauten nun wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c7f87-105">The **Material** objects now read as follows:</span></span>


```
Material RedMaterial {
1.000000;0.000000;0.000000;1.000000;;    // R = 1.0, G = 0.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
TextureFilename { "tex1.ppm"; }
}

Material GreenMaterial {
0.000000;1.000000;0.000000;1.000000;;     // R = 0.0, G = 1.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
TextureFilename { "win95.ppm"; }
}
```



## <a name="related-topics"></a><span data-ttu-id="c7f87-106">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7f87-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7f87-107">X-Dateien (Legacy)</span><span class="sxs-lookup"><span data-stu-id="c7f87-107">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



