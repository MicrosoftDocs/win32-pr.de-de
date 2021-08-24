---
title: label – im Vergleich zu
description: Markieren Sie die nächste Anweisung mit einem Bezeichnungsindex. | label – im Vergleich zu
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81c36c3db93acdc82d725c9cf7893c52d7177bbe70e16378c3b86f39ec4d6a2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854180"
---
# <a name="label---vs"></a>label – im Vergleich zu

Markieren Sie die nächste Anweisung mit einem Bezeichnungsindex.

## <a name="syntax"></a>Syntax



| Label l\# |
|-----------|



 

, wobei \# die Bezeichnungsnummer identifiziert.

Bei vs \_ 2 \_ 0 und vs \_ 2 \_ x muss die Bezeichnungsnummer zwischen 0 und 15 sein.

Bei vs \_ 2 \_ sw, vs \_ 3 \_ 0 und vs \_ 3 \_ sw muss die Bezeichnungsnummer zwischen 0 und 2047 sein.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| label                  |      | x    | x    | x     | x    | x     |



 

Diese Anweisung definiert eine Bezeichnung, die sich in der nächsten Shaderanweisung befindet. Die Bezeichnungsanweisung kann nur direkt nach einer [ret-Anweisung](ret---vs.md) vorhanden sein (die das Ende der vorherigen Unterroutine oder des Hauptprogramms definiert).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




