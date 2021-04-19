---
description: Ein float-Wert, der den aktuellen parametrischen Endpunkt für den Strahl darstellt.
ms.assetid: ''
title: Raycurrent
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTCurrent
api_type:
- NA
ms.openlocfilehash: 4f090bab88c6be671ca0614255fd7bdebb0d1549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342773"
---
# <a name="raytcurrent"></a>Raycurrent

Ein float-Wert, der den aktuellen parametrischen Endpunkt für den Strahl darstellt.  

## <a name="syntax"></a>Syntax

```
float RayTCurrent();

```


## <a name="remarks"></a>Bemerkungen

**Raytcurrent** definiert den aktuellen Endpunkt des Strahls gemäß der folgenden Formel: Origin + (Direction * raytcurrent).  Der *Ursprung* und die *Richtung* können sich entweder in der Welt oder im Objektbereich befinden, was zu einer Welt-oder einem Objekt Raum Endpunkt führt.

" **Raytcurrent** " wird im Aufrufe " [**traceray**](traceray-function.md) " mit dem Wert " [**raydebug:: TMAX**](raydesc.md) " initialisiert und anschließend während der Ablauf Verfolgungs Abfrage aktualisiert, wenn interabschnitte gemeldet werden (in jedem beliebigen Treffer) und akzeptiert werden.

Im [Schnittpunkt-Shader](intersection-shader.md)stellt Sie den Abstand zum nächstgelegenen Schnittpunkt dar, der bisher gefunden wurde.  Der Wert wird nach () auf den Thit-Wert aktualisiert, sofern der Treffer akzeptiert wurde.

Im [beliebigen Treffer-Shader](any-hit-shader.md)stellt Sie den Abstand zur aktuellen Schnittmenge dar, die gemeldet wird.

Im [nächsten Treffer-Shader](closest-hit-shader.md)stellt Sie den Abstand zur nächstgelegenen Schnittmenge dar, die akzeptiert wird.

Im [fehl-Shader](miss-shader.md)ist es gleich *TMAX* , das an den **traceray** -Befehl übergeben wird.


Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)
* [**Miss-Shader**](miss-shader.md)





## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




