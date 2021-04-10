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
# <a name="adding-textures-direct3d-9"></a>Hinzufügen von Texturen (Direct3D 9)

Verwenden Sie zum Hinzufügen von Texturen die hierarchische Natur des Datei Formats, und fügen Sie den [**Material**](material.md) Datenobjekten ein optionales [**texturefilename**](texturefilename.md) -Datenobjekt hinzu. Die **Material** -Objekte lauten nun wie folgt:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X-Dateien (Legacy)](x-files--legacy-.md)
</dt> </dl>

 

 



