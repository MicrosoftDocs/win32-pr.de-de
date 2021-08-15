---
description: Definiert eine grundlegende Materialfarbe, die entweder auf ein vollständiges Gitternetz oder auf die einzelnen Gesichter eines Gitters angewendet werden kann. Die Potenz ist der Glanz exponent des Materials.
ms.assetid: vs|directx_sdk|~\material.htm
title: Material
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d4dcb1cef7597ff7c02d16f1db311287511166c9259c89a0ea60a0c49fb7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798967"
---
# <a name="material"></a>Material

Definiert eine grundlegende Materialfarbe, die entweder auf ein vollständiges Gitternetz oder auf die einzelnen Gesichter eines Gitters angewendet werden kann. Die Potenz ist der Glanz exponent des Materials.

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

Hierbei gilt:

-   faceColor: Gesichtsfarbe. Eine ColorRGBA-Vorlage. Weitere Informationen finden Sie unter [**ColorRGBA**](colorrgba.md).
-   power : Material specular color exponent.
-   specularColor: Material specular color. Eine ColorRGB-Vorlage. Weitere Informationen finden Sie unter [**ColorRGB**](colorrgb.md).
-   emissiveColor: Materialemissive Farbe. Eine ColorRGB-Vorlage. Weitere Informationen finden Sie unter [**ColorRGB**](colorrgb.md).

> [!Note]  
> Die Umgebungsfarbe erfordert eine Alphakomponente.

 

[**TextureFilename**](texturefilename.md) ist ein optionales Datenobjekt. Wenn dieses Objekt nicht vorhanden ist, wird das Gesicht nicht textiert.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



