---
description: Definiert einen Satz von zwei booleschen Werten, die in der meshfacewrapper-Vorlage verwendet werden, um die Textur Topologie eines einzelnen Gesichts zu definieren. Verwenden Sie anstelle von Boolean2d, wenn die Texturkoordinaten (u, v) den Bereich von 0 bis 2 anstelle von 0 bis 1 umfassen.
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: Materialwrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6797719919a4f52421751a5cad008aa8a581089a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340066"
---
# <a name="materialwrap"></a>Materialwrap

Definiert einen Satz von zwei booleschen Werten, die in der [**meshfacewrapper**](meshfacewraps.md) -Vorlage verwendet werden, um die Textur Topologie eines einzelnen Gesichts zu definieren. Verwenden Sie anstelle von [**Boolean2d**](boolean2d.md) , wenn die Texturkoordinaten (u, v) den Bereich von 0 bis 2 anstelle von 0 bis 1 umfassen.

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

Hierbei gilt:

-   u-boolescher Wert. Siehe [**Boolean**](boolean.md).
-   v-boolescher Wert. Siehe [**Boolean**](boolean.md).

> [!Note]  
> Die Vorlage " [**meshfacewrapper**](meshfacewraps.md) " wird nicht mehr verwendet.

 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



