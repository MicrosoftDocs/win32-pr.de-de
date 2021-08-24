---
title: label – ps
description: Markieren Sie die nächste Anweisung als Bezeichnungsindex. | label – ps
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 921abbc0518182eaef17326082a395e5c5729d8ab550610fe71c8dfabe46dd4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854200"
---
# <a name="label---ps"></a>label – ps

Markieren Sie die nächste Anweisung als Bezeichnungsindex.

## <a name="syntax"></a>Syntax



| label l\# |
|-----------|



 

wobei \# die Bezeichnungsnummer identifiziert.

Für PS \_ 2 \_ x muss die Bezeichnungsnummer zwischen 0 und 15 liegen.

Für ps 2 sw, ps 3 0 und ps 3 sw muss die Bezeichnungsnummer zwischen 0 und \_ \_ \_ \_ \_ \_ 2047 liegen.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| label                 |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung definiert eine Bezeichnung, die sich in der nächsten Shaderanweisung befindet. Die Bezeichnungsanweisung kann nur direkt nach einer [ret-Anweisung](ret---ps.md) vorhanden sein (die das Ende der vorherigen Unterroutine oder des Hauptprogramms definiert).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




