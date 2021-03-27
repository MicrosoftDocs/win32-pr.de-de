---
title: DST-vs
description: Berechnet einen Entfernungs Vektor. | DST-vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e41c1da0eae001d314e2682a3295a0b88b993ee1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103869727"
---
# <a name="dst---vs"></a>DST-vs

Berechnet einen Entfernungs Vektor.

## <a name="syntax"></a>Syntax



| DST dest, src0, Quelle1 |
|----------------------|



 

where

-   dest ist das Ziel Register.
-   src0 ist ein Quell Register.
-   Quelle1 ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| DST                    | x    | x    | x    | x     | x    | x     |



 

Das folgende Code Fragment zeigt die Vorgänge, die ausgeführt werden:


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



Der erste Quell Operand (src0) wird als Vektor angenommen (ignoriert, d \* d, d, \* ignoriert), und der zweite Quell Operand (Quelle1) wird als Vektor angenommen (ignoriert, 1/d, ignoriert, 1/d). Das Ziel (dest) ist der Ergebnis Vektor (1, d, d \* d, 1/d).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




