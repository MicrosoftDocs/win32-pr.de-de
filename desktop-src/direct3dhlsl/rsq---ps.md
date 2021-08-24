---
title: rsq – ps
description: Berechnet die reziproke Quadratwurzel (nur positiv) des Quellskalars. | rsq – ps
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 48a36715113678e199b3da22be9cdf118f385c15397a16ddd39bdd83622f76f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788700"
---
# <a name="rsq---ps"></a>rsq – ps

Berechnet die reziproke Quadratwurzel (nur positiv) des Quellskalars.

## <a name="syntax"></a>Syntax



| rsq dst, src |
|--------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister. Das Quellregister erfordert die explizite Verwendung von "replicate swizzle", d.h. genau eine der .x-, .y-, .z-, .w swizzle-Komponenten (oder die Entsprechungen .r, .g, .b, .a) muss angegeben werden.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| rsq                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Der absolute Wert wird vor der Verarbeitung übernommen.

Die Genauigkeit sollte mindestens 1,0/(2): absoluter Fehler über dem Bereich (1,0, 4,0) sein, da allgemeine Implementierungen Mantisse und Exponent trennen.

Die Ausgabe muss genau 1,0 sein, wenn die Eingabe genau 1,0 ist. Eine Quelle von 0,0 ergibt unendlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




