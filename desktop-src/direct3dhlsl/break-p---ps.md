---
title: breakp-PS
description: Unterbrechen Sie die aktuelle Schleife bedingt bei den nächstgelegenen ENDLOOP-PS oder ENDREP-PS. Verwenden Sie eine der Komponenten des Prädikats "Register" als Bedingung, um zu bestimmen, ob die Anweisung durchgeführt werden soll.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389551"
---
# <a name="breakp---ps"></a>breakp-PS

Unterbrechen Sie die aktuelle Schleife bedingt bei den nächstgelegenen [ENDLOOP-PS](endloop---ps.md) oder [ENDREP-PS](endrep---ps.md). Verwenden Sie eine der Komponenten des Prädikats "Register" als Bedingung, um zu bestimmen, ob die Anweisung durchgeführt werden soll.

## <a name="syntax"></a>Syntax



| Break p \[ ! \] P0. Stuben|Teenie|z|Löw |
|-----------------------------|



 

Hierbei gilt:

-   \[!\] ist ein optionaler Negation-Modifizierer.
-   P0 ist das [Prädikat Register](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} ist das erforderliche Replizieren von Replizieren auf p0.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Break p                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




