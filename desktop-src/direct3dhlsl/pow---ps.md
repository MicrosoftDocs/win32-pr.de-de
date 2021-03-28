---
title: Pow-PS
description: Abs (src0) mit vollständiger Genauigkeit Quelle1. | Pow-PS
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981272"
---
# <a name="pow---ps"></a>Pow-PS

Abs (src0) mit vollständiger Genauigkeit<sup>Quelle1</sup>.

## <a name="syntax"></a>Syntax



| Pow DST, src0, Quelle1 |
|---------------------|



 

where

-   DST ist das Ziel Register.
-   src0 ist ein Eingabe Quellen Register. Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.
-   Quelle1 ist ein Eingabe Quellen Register. Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| pow                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Diese Anweisung funktioniert wie folgt:

dest. x = dest. y = dest. z = dest. w = \[ Abs (src0) \] <sup>Quelle1</sup>;

Dabei handelt es sich um eine skalare Anweisung. Daher sollten die Quell Register über repliziert werden, um anzugeben, welche Kanäle verwendet werden.

Die Eingabe Potenz (Quelle1) muss ein Skalar sein.

Das skalare Ergebnis wird in alle vier Ausgabekanäle repliziert.

Diese Anweisung kann als Exp (Quelle1 \* Log (src0)) erweitert werden.

Das DST-Register muss ein temporäres Register sein und sollte nicht dasselbe Register wie Quelle1 sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




