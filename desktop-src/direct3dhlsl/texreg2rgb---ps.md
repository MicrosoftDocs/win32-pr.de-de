---
title: texreg2rgb-PS
description: Interpretiert die roten, grünen und blauen (RGB) Farbkomponenten des Quell Registers als Textur Adressdaten, um die Textur in der Phase zu testen, die der Ziel Registernummer entspricht. Das Ergebnis wird im Ziel Register gespeichert.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8bcd2bbd7e57ba9dc692f34404a5610cdc517f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516496"
---
# <a name="texreg2rgb---ps"></a>texreg2rgb-PS

Interpretiert die roten, grünen und blauen (RGB) Farbkomponenten des Quell Registers als Textur Adressdaten, um die Textur in der Phase zu testen, die der Ziel Registernummer entspricht. Das Ergebnis wird im Ziel Register gespeichert.

## <a name="syntax"></a>Syntax



| texreg2rgb DST, src |
|---------------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texreg2rgb            |      | x    | x    |      |      |      |       |      |       |



 

Diese Anweisung ist für die Neuzuordnung von Farbräumen nützlich. Es unterstützt zweidimensionale (2D) und dreidimensionale (3D) Koordinaten. Sie kann wie [texreg2ar-PS](texreg2ar---ps.md) oder [texreg2gb-PS](texreg2gb---ps.md) verwendet werden, um 2D-Daten neu zuzuordnen. Diese Anweisung unterstützt jedoch auch 3D-Daten, sodass Sie mit Cubemaps und 3D-volumetexturen verwendet werden kann.

Im folgenden finden Sie ein Beispiel für die Sequenz, auf die die Anweisung folgt.


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



Im folgenden finden Sie weitere Details dazu, wie die Neuzuordnung erreicht wird.

<dl> Die erste Anweisung lädt die Textur Farbe (RGBA) in das Register TN.  
tex TN  
Mit der zweiten Anweisung wird die Farbe neu zugeordnet.  
t (m)<sub>RGBA</sub> = texturesample (Phase m)<sub>RGBA</sub> mit t (n)<sub>RGB</sub> als Koordinaten
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




