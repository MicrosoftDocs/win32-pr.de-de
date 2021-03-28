---
title: RSQ-PS
description: Berechnet die gegenseitige Quadratwurzel (nur positiv) des Quell Skalars. | RSQ-PS
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13777810c67ba38b2c8f47f0c0db0cf9b70771ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981552"
---
# <a name="rsq---ps"></a>RSQ-PS

Berechnet die gegenseitige Quadratwurzel (nur positiv) des Quell Skalars.

## <a name="syntax"></a>Syntax



| RSQ DST, src |
|--------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register. Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| RSQ                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Der absolute Wert wird vor der Verarbeitung übernommen.

Die Genauigkeit muss mindestens 1.0/(2 ² ²) absolute Fehler im Bereich (1,0, 4,0) betragen, da allgemeine Implementierungen die Mantisse und den Exponenten voneinander trennen.

Die Ausgabe muss genau 1,0 sein, wenn die Eingabe genau 1,0 ist. Eine Quelle von 0,0 ergibt unendlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




