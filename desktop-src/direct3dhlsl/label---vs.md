---
title: Bezeichnung (VS)
description: Markieren Sie die nächste Anweisung mit einem Bezeichnungs Index. | Bezeichnung (VS)
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e2b72fe21301aa66d8428dc3696ceb3f12e6214
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995722"
---
# <a name="label---vs"></a>Bezeichnung (VS)

Markieren Sie die nächste Anweisung mit einem Bezeichnungs Index.

## <a name="syntax"></a>Syntax



| Bezeichnung l\# |
|-----------|



 

Gibt an, wo die Bezeichnungs \# Nummer identifiziert.

Für vs \_ 2 \_ 0 und vs \_ 2 \_ x muss die Bezeichnungs Nummer zwischen 0 und 15 liegen.

Für vs \_ 2 \_ SW, vs \_ 3 \_ 0 und vs \_ 3 \_ SW, muss die Nummer der Bezeichnung zwischen 0 und 2047 liegen.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| label                  |      | x    | x    | x     | x    | x     |



 

Diese Anweisung definiert eine Bezeichnung, die sich in der nächsten shaderanweisung befindet. Die Bezeichnungs Anweisung kann nur direkt nach einer [ret](ret---vs.md) -Anweisung vorhanden sein (die das Ende der vorherigen Unterroutine oder des Hauptprogramms definiert).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




