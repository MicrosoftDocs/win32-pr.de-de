---
title: texdp3 – ps
description: Führt ein Drei-Komponenten-Punktprodukt zwischen Daten in der Texturregisternummer und dem Texturkoordinatensatz aus, der der Zielregisternummer entspricht.
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e39f2682aac7741af304269b0584f3552158b2f83596c7fd55f1c83948d09f0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788200"
---
# <a name="texdp3---ps"></a>texdp3 – ps

Führt ein Drei-Komponenten-Punktprodukt zwischen Daten in der Texturregisternummer und dem Texturkoordinatensatz aus, der der Zielregisternummer entspricht.

## <a name="syntax"></a>Syntax



| texdp3 dst, src |
|-----------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3                |      | x    | x    |      |      |      |       |      |       |



 

Texturregister müssen die folgende Sequenz verwenden.


```
 
tex    t(n)        // Define tn as a standard 3-vector (tn must be 
                   //   defined in some way before texdp3 uses it)
texdp3 t(m), t(n)  // where m > n
                   // Perform a three-component dot product between tn and 
                   //   the texture coordinate set m. The scalar result is
                   //   replicated to all components of t(m)
```



Im Folgenden finden Sie weitere Details dazu, wie das Punktprodukt erreicht wird.

Die texdp3-Anweisung führt ein aus drei Komponenten orientiertes Punktprodukt aus und repliziert es auf alle vier Farbkanäle.

t(m)<sub>RGBA</sub> = TextureCoordinates(Stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




