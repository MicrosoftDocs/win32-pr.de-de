---
title: dst – vs
description: Berechnet einen Entfernungsvektor. | dst – vs
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d75eb61dd498d7a2f1d6bd9c5bd0dd9c52f3fd56625cb41b0026e9acce431ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068350"
---
# <a name="dst---vs"></a>dst – vs

Berechnet einen Entfernungsvektor.

## <a name="syntax"></a>Syntax



| dst dest, src0, src1 |
|----------------------|



 

where

-   dest ist das Zielregister.
-   src0 ist ein Quellregister.
-   src1 ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dst                    | x    | x    | x    | x     | x    | x     |



 

Das folgende Codefragment zeigt die ausgeführten Vorgänge:


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



Es wird davon ausgegangen, dass der erste Quellopernd (src0) der Vektor ist (ignoriert, d, d, d, ignoriert), und der zweite Quellopernd (src1) wird als Vektor angenommen \* \* (ignoriert, 1/d, ignoriert, 1/d). Das Ziel (dest) ist der Ergebnisvektor (1, d, \* d d, 1/d).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




