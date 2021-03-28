---
title: Break p-vs
description: Unterbrechen Sie die aktuelle Schleife bedingt bei den nächstgelegenen ENDLOOP-vs oder ENDREP-vs. verwenden Sie eine der Komponenten des Prädikats als Bedingung, um zu bestimmen, ob die Anweisung durchgeführt werden soll oder nicht.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038334"
---
# <a name="breakp---vs"></a>Break p-vs

Unterbrechen Sie die aktuelle Schleife bedingt bei den nächstgelegenen [endschleifen-vs](endloop---vs.md) oder [ENDREP-vs](endrep---vs.md). Verwenden Sie eine der Komponenten des Prädikats "Register" als Bedingung, um zu bestimmen, ob die Anweisung durchgeführt werden soll.

## <a name="syntax"></a>Syntax



| Break p \[ ! \] P0. Stuben|Teenie|z|Löw |
|-----------------------------|



 

Hierbei gilt:

-   \[!\] Optionaler boolescher Wert nicht.
-   P0 ist das Prädikat Register. Siehe [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} ist das erforderliche Replizieren von Replizieren auf p0.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Break p                 |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




