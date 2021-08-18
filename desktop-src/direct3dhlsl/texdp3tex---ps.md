---
title: texdp3tex – ps
description: Führt ein Punktprodukt mit drei Komponenten aus und verwendet das Ergebnis für eine 1D-Textursuche.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91014b52b04417bbb23e76988beeb0bd4c473bd1e1d116433a8fd1dbf09a47ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788036"
---
# <a name="texdp3tex---ps"></a>texdp3tex – ps

Führt ein Punktprodukt mit drei Komponenten aus und verwendet das Ergebnis für eine 1D-Textursuche.

## <a name="syntax"></a>Syntax



| texdp3tex dst, src |
|--------------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3tex             |      | x    | x    |      |      |      |       |      |       |



 

Texturregister müssen die folgende Sequenz verwenden.


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



Hier finden Sie weitere Details dazu, wie das Punktprodukt und die Textursuche durchgeführt werden.

Die texdp3tex-Anweisung führt ein Punktprodukt mit drei Komponenten aus.

u' = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Das Ergebnis wird verwendet, um die Textur in der Texturphase m zu untersuchen, indem eine 1D-Suche durchgeführt wird.

t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using (u',0,0) as coordinates

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




