---
title: dp3 – ps
description: Berechnet das Drei-Komponenten-Punktprodukt der Quellregister. | dp3 – ps
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49e957078832f11885ea82baf8438d712394133eb77ad8eeaba705ff0d32a9d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024630"
---
# <a name="dp3---ps"></a>dp3 – ps

Berechnet das Drei-Komponenten-Punktprodukt der Quellregister.

## <a name="syntax"></a>Syntax



| dp3 dst, src0, src1 |
|---------------------|



 

where

-   dst ist das Zielregister.
-   src0 ist ein Quellregister.
-   src1 ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp3                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Der folgende Codeausschnitt zeigt die ausgeführten Vorgänge:


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



Diese Anweisung wird in der Vektorpipeline ausgeführt und schreibt immer in die Farbkanäle. Für Version 1 4 verwendet diese Anweisung weiterhin die \_ Vektorpipeline, kann aber in einen beliebigen Kanal schreiben.

Eine Anweisung mit einer RGB-Schreibmaske (.xyz) für das Zielregister kann mit dp3 gemeinsam ausgegeben werden, wie unten gezeigt.


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



Die dp3-Anweisung kann [](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) mit dem Eingabeargumentmodifizierer für die signierte Skalierung des Quellregisters ( bx2) geändert werden, der auf die Eingabeargumente angewendet wird, wenn sie nicht bereits auf den signierten dynamischen \_ Bereich erweitert sind. Bei einem Beleuchtungs-Shader wird häufig der Modifizierer für die Saturate-Anweisung (Sat) verwendet, um die negativen Werte an Schwarz zu klammern, wie \_ im folgenden Beispiel gezeigt.


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




