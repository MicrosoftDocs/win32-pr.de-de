---
title: texreg2rgb – ps
description: Interpretiert die Farbkomponenten rot, grün und blau (RGB) des Quellregisters als Texturadressendaten, um die Textur in der Stufe zu erfassen, die der Zielregisternummer entspricht. Das Ergebnis wird im Zielregister gespeichert.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c32ee8e6b1560bfcebf6a914a45be2c74b19e94568c9d4e9b24084bf56c3f01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043048"
---
# <a name="texreg2rgb---ps"></a>texreg2rgb – ps

Interpretiert die Farbkomponenten rot, grün und blau (RGB) des Quellregisters als Texturadressendaten, um die Textur in der Stufe zu erfassen, die der Zielregisternummer entspricht. Das Ergebnis wird im Zielregister gespeichert.

## <a name="syntax"></a>Syntax



| texreg2rgb dst, src |
|---------------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2rgb            |      | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung ist nützlich für Neuzuordnungsvorgänge im Farbraum. Es unterstützt zweidimensionale (2D) und dreidimensionale Koordinaten (3D). Sie kann genau wie die [texreg2ar - ps](texreg2ar---ps.md) oder [texreg2gb - ps](texreg2gb---ps.md) verwendet werden, um 2D-Daten neu zuzuordnen. Diese Anweisung unterstützt jedoch auch 3D-Daten, sodass sie mit Cube maps und 3D-Volumentexturen verwendet werden können.

Hier sehen Sie ein Beispiel für die Sequenz, auf die die Anweisung folgt.


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



Hier finden Sie weitere Details zur Durchführung der Neuzuordnung.

<dl> Die erste Anweisung lädt die Texturfarbe (RGBA) in das Register tn.  
tex tn  
Die zweite Anweisung weist die Farbe neu zu  
t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> mit t(n)<sub>RGB</sub> als Koordinaten
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




