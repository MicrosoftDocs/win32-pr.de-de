---
title: texdp3-PS
description: Führt ein 3-Komponenten-Punktprodukt zwischen den Daten in der Textur Registernummer und dem Texturkoordinaten Satz aus, der der Ziel Registernummer entspricht.
ms.assetid: 82e02f3f-4b88-4007-b4be-0c66223d9c66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 64cc14ee66123ea3e25941579b9838977a753174
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313619"
---
# <a name="texdp3---ps"></a>texdp3-PS

Führt ein 3-Komponenten-Punktprodukt zwischen den Daten in der Textur Registernummer und dem Texturkoordinaten Satz aus, der der Ziel Registernummer entspricht.

## <a name="syntax"></a>Syntax



| texdp3 DST, src |
|-----------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3                |      | x    | x    |      |      |      |       |      |       |



 

Textur Register müssen die folgende Sequenz verwenden.


```
 
tex    t(n)        // Define tn as a standard 3-vector (tn must be 
                   //   defined in some way before texdp3 uses it)
texdp3 t(m), t(n)  // where m > n
                   // Perform a three-component dot product between tn and 
                   //   the texture coordinate set m. The scalar result is
                   //   replicated to all components of t(m)
```



Im folgenden finden Sie weitere Details dazu, wie das Punktprodukt erreicht wird.

Die texdp3-Anweisung führt ein 3-Komponenten-Punktprodukt aus und repliziert es in alle vier Farbkanäle.

t (m)<sub>RGBA</sub> = TextureCoordinates (Stufe m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




