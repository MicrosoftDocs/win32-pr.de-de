---
title: breakp – ps
description: Bedingtes Unterbrechen der aktuellen Schleife am nächsten Endeloop – ps oder endrep – ps. Verwenden Sie eine der Komponenten des Prädikatregisters als Bedingung, um zu bestimmen, ob die Anweisung ausgeführt werden soll.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2da0d2bceea7a3e44f02e6b732337cb3447d6ef1c9798f95b664bf4da96ec2dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983320"
---
# <a name="breakp---ps"></a>breakp – ps

Unterbrechen Sie die aktuelle Schleife bedingt am nächstgelegenen [endloop - ps](endloop---ps.md) oder [endrep - ps](endrep---ps.md). Verwenden Sie eine der Komponenten des Prädikatregisters als Bedingung, um zu bestimmen, ob die Anweisung ausgeführt werden soll.

## <a name="syntax"></a>Syntax



| breakp \[ ! \] p0. {x\|y\|z\|w} |
|-----------------------------|



 

Hierbei gilt:

-   \[!\] ist ein optionaler Negationmodifizierer.
-   p0 ist das [Prädikatregister.](dx9-graphics-reference-asm-ps-registers-predicate.md)
-   {x \| y \| z \| w} ist die erforderliche Replikationswizzle auf p0.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Breakp                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




