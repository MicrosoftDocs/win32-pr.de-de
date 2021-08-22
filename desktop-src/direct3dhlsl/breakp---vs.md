---
title: breakp – vs
description: Bedingtes Unterbrechen der aktuellen Schleife am nächsten Endeloop – vs oder endrep – vs. Verwenden Sie eine der Komponenten des Prädikatregisters als Bedingung, um zu bestimmen, ob die Anweisung ausgeführt werden soll.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a768acaecaa77a42990b34c50cd8eccb24d61353550751f3ed830e7844d7624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794314"
---
# <a name="breakp---vs"></a>breakp – vs

Bedingtes Unterbrechen der aktuellen Schleife am nächsten [Endeloop – vs oder](endloop---vs.md) [endrep – vs](endrep---vs.md). Verwenden Sie eine der Komponenten des Prädikatregisters als Bedingung, um zu bestimmen, ob die Anweisung ausgeführt werden soll.

## <a name="syntax"></a>Syntax



| breakp \[ ! \] p0. {x\|y\|z\|w} |
|-----------------------------|



 

Hierbei gilt:

-   \[!\] Optionaler boolescher WERT NOT.
-   p0 ist das Prädikatregister. Weitere Informationen finden Sie unter [Prädikatregister.](dx9-graphics-reference-asm-vs-registers-predicate.md)
-   {x \| y \| z \| w} ist die erforderliche Replikationswizzle auf p0.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Breakp                 |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




