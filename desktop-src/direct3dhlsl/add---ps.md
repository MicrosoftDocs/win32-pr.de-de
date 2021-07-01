---
title: add - ps
description: Fügt zwei Vektoren hinzu. | add - ps
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54092caf19a486b68b92ef63d992f11289a51c93
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130089"
---
# <a name="add---ps"></a>add - ps

Fügt zwei Vektoren hinzu.

## <a name="syntax"></a>Syntax



| add dst, src0, src1 |
|---------------------|



 

where

-   dst ist das Zielregister.
-   src0 ist ein Quellregister.
-   src1 ist ein Quellregister.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| add                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Der folgende Codeausschnitt zeigt die ausgeführten Vorgänge.


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a>Anweisungsinformationen



|   Anforderung                       | Wert           |
|--------------------------|------------|
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen zum Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




