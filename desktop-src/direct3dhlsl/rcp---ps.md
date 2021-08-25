---
title: rcp – ps
description: Berechnet den Kehrwert des Quellskalars. | rcp – ps
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fba443d4a2e05794f8c1965e46a61c65edae50b95845f0f80faa0c0ab6c6bf71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510955"
---
# <a name="rcp---ps"></a>rcp – ps

Berechnet den Kehrwert des Quellskalars.

## <a name="syntax"></a>Syntax



| rcp dst, src |
|--------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister. Das Quellregister erfordert die explizite Verwendung von "replicate swizzle", d.h. genau eine der .x-, .y-, .z-, .w swizzle-Komponenten (oder die Entsprechungen .r, .g, .b, .a) muss angegeben werden.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| rcp                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Die Ausgabe muss genau 1,0 sein, wenn die Eingabe genau 1,0 ist. Eine Quelle von 0,0 ergibt unendlich.

Das skalare Ergebnis wird in alle Kanäle in der Ziel-Schreibmaske repliziert.

Die Genauigkeit sollte mindestens 1,0/(2): absoluter Fehler über dem Bereich (1,0, 2,0) sein, da allgemeine Implementierungen Mantisse und Exponent trennen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




