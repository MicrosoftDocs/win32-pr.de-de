---
description: Ein Gleitkommawert, der den aktuellen parametrischen Startpunkt für den Strahl darstellt.
ms.assetid: ''
title: RayTMin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 5429574480cfda071dfec93cea771211bab578bdaecb4513c76f43c4d820b22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989480"
---
# <a name="raytmin"></a>RayTMin

Ein Gleitkommawert, der den aktuellen parametrischen Startpunkt für den Strahl darstellt. 

## <a name="syntax"></a>Syntax

```
float RayTMin();

```

## <a name="remarks"></a>Hinweise

**RayTMin** definiert den Startpunkt des Strahls gemäß der folgenden Formel: Origin + (Direction * RayTMin).  *Ursprung* und *Richtung* können sich entweder im Welt- oder Objektbereich bewegen, was entweder zu einem Ausgangspunkt für eine Welt oder einen Objektbereich führt.

**RayTMin** wird im Aufruf von [**TraceRay**](traceray-function.md)angegeben und ist für die Dauer dieses Aufrufs konstant.




Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)
* [**Miss-Shader**](miss-shader.md)





## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




