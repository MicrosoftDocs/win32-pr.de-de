---
title: texdp3tex-PS
description: Führt ein 3-Komponenten-Punktprodukt aus und verwendet das Ergebnis, um eine 1D-Textur Suche durchzuführen.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dfe74dd0a73bc47cd2855d35b239e80a1b5153c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992975"
---
# <a name="texdp3tex---ps"></a>texdp3tex-PS

Führt ein 3-Komponenten-Punktprodukt aus und verwendet das Ergebnis, um eine 1D-Textur Suche durchzuführen.

## <a name="syntax"></a>Syntax



| texdp3tex DST, src |
|--------------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texdp3tex             |      | x    | x    |      |      |      |       |      |       |



 

Textur Register müssen die folgende Sequenz verwenden.


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



Hier finden Sie weitere Details dazu, wie das Punktprodukt und die Textur Suche durchgeführt werden.

Die texdp3tex-Anweisung führt ein 3-Komponenten-Punktprodukt aus.

u ' = TextureCoordinates (Stufe m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Das Ergebnis wird verwendet, um eine Stichprobe der Textur in Textur Phase m Durchführen einer 1D-Suche durchzuführen.

t (m)<sub>RGBA</sub> = texturesample (Phase m)<sub>RGBA</sub> mit (u ', 0, 0) als Koordinaten

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




