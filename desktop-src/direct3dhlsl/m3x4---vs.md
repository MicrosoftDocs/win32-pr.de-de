---
title: M3x4-vs
description: Multipliziert einen 3-Komponenten Vektor mit einer rund m3-Matrix. | M3x4-vs
ms.assetid: 8bec1ac5-376b-4eae-ba82-b42a6c0e7c4e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4018698dbe6ab986945a84c1fcf9ce0431bd0fc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981305"
---
# <a name="m3x4---vs"></a>M3x4-vs

Multipliziert einen 3-Komponenten Vektor mit einer rund m3-Matrix.

## <a name="syntax"></a>Syntax



| M3x4 DST, src0, Quelle1 |
|----------------------|



 

where

-   DST ist das Ziel Register. Das Ergebnis ist ein Vektor mit 4 Komponenten.
-   src0 ist ein Quell Register, das einen 3-Komponenten Vektor darstellt.
-   Quelle1 ist ein Quell Register, das eine rund m3-Matrix darstellt, die dem ersten von vier aufeinander folgenden Registern entspricht.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| m3x4                   | x    | x    | x    | x     | x    | x     |



 

Die xyzw-Maske (Standard) ist für das Ziel Register erforderlich. Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.

Das folgende Code Fragment zeigt die ausgeführten Vorgänge.


```
 
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z);
```



Der Eingabe Vektor befindet sich im Register src0. Die rund m3-Eingabe Matrix befindet sich in Register Quelle1 und die nächsten drei höheren Register, wie in der folgenden Erweiterung gezeigt.

Dieser Vorgang wird häufig verwendet, um einen Positions Vektor durch eine Matrix zu transformieren, die einen projectiven Effekt hat, aber keine Übersetzung anwendet. Diese Anweisung wird als Paar von Punkt Produkten implementiert, wie hier gezeigt.


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




