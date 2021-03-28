---
title: Bem-PS
description: Anwenden einer gefälschten Bump Environment-Map-Transformation.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7c591555e2cbd2c6eaebf6e392bb94d6ec50e748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389560"
---
# <a name="bem---ps"></a>Bem-PS

Anwenden einer gefälschten Bump Environment-Map-Transformation.

## <a name="syntax"></a>Syntax



| Bem DST. RG, src0, Quelle1 |
|------------------------|



 

where

-   DST. RG DST ist das Ziel Register. Die rote und grüne Komponenten Schreib Maske muss verwendet werden.
-   src0 ist ein Quell Register.
-   Quelle1 ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Bem                   |      |      |      | x    |      |      |       |      |       |



 

Diese Anweisung führt die folgende Berechnung aus.


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



Regeln für die Verwendung von Bem:

1.  Bem muss in der ersten Phase eines Shaders (d. h. vor einem Phasen Marker) angezeigt werden.
2.  Bem verwendet zwei arithmetische Anweisungs Slots.
3.  Nur eine Verwendung dieser Anweisung ist pro Shader zulässig.
4.  Die Ziel-schreibfrage muss ". RG/.XY." lauten.
5.  Diese Anweisung kann nicht gemeinsam ausgegeben werden.
6.  Abgesehen von der Einschränkung, dass die Ziel Schreib Maske. RG ist, sind Modifizierer für die Quell-src0-, Quelle1-und Anweisungs Modifizierer nicht eingeschränkt.

## <a name="instruction-information"></a>Anweisungs Informationen



|                          |            |
|--------------------------|------------|
| Mindestens Betriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




