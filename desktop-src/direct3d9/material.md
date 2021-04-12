---
description: Definiert eine grundlegende Material Farbe, die entweder auf ein ganzes Mesh oder auf die einzelnen Flächen eines Netzes angewendet werden kann. Die Stromversorgung ist der Glanz Exponent des Materials.
ms.assetid: vs|directx_sdk|~\material.htm
title: Material
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480702"
---
# <a name="material"></a>Material

Definiert eine grundlegende Material Farbe, die entweder auf ein ganzes Mesh oder auf die einzelnen Flächen eines Netzes angewendet werden kann. Die Stromversorgung ist der Glanz Exponent des Materials.

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

-   fakecolor-Vordergrundfarbe. Eine colorrgba-Vorlage. Siehe [**colorrgba**](colorrgba.md).
-   Glanz Farben-Exponent für Energie Material.
-   SpecularColor-Material Glanz Farbe. Eine colorrgb-Vorlage. Siehe [**colorrgb**](colorrgb.md).
-   emissivecolor-Material selbst leuchtendes Color. Eine colorrgb-Vorlage. Siehe [**colorrgb**](colorrgb.md).

> [!Note]  
> Die Umgebungs Farbe erfordert eine Alpha Komponente.

 

[**Texturefilename**](texturefilename.md) ist ein optionales Datenobjekt. Wenn dieses Objekt nicht vorhanden ist, wird das Gesicht nicht texturiert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



