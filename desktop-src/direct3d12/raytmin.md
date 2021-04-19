---
description: Ein float-Wert, der den aktuellen parametrischen Anfangspunkt für den Strahl darstellt.
ms.assetid: ''
title: Raytmin
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
ms.openlocfilehash: 00db0eb46e8c011e5b31f773679e19ca6dd4a7a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346450"
---
# <a name="raytmin"></a>Raytmin

Ein float-Wert, der den aktuellen parametrischen Anfangspunkt für den Strahl darstellt. 

## <a name="syntax"></a>Syntax

```
float RayTMin();

```

## <a name="remarks"></a>Bemerkungen

**Raytmin** definiert den Anfangspunkt des Strahls gemäß der folgenden Formel: Origin + (Direction * raytmin).  Der *Ursprung* und die *Richtung* können sich entweder in der Welt oder im Objektbereich befinden, was zu einem Ausgangspunkt der Welt oder einem Objektbereich führt.

**Raytmin** wird im Aufrufe von [**traceray**](traceray-function.md)angegeben und ist für die Dauer des Aufrufes konstant.




Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)
* [**Miss-Shader**](miss-shader.md)





## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




