---
title: Bezeichnung-PS
description: Markieren Sie die nächste Anweisung mit einem Bezeichnungs Index. | Bezeichnung-PS
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3fb266b649642c82293e8310b6302c6763ddc27
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995575"
---
# <a name="label---ps"></a>Bezeichnung-PS

Markieren Sie die nächste Anweisung mit einem Bezeichnungs Index.

## <a name="syntax"></a>Syntax



| Bezeichnung l\# |
|-----------|



 

Gibt an, wo die Bezeichnungs \# Nummer identifiziert.

Für PS \_ 2 \_ x muss die Bezeichnungs Nummer zwischen 0 und 15 liegen.

Für PS \_ 2 \_ SW, PS \_ 3 \_ 0 und PS \_ 3 \_ SW muss die Bezeichnungs Nummer zwischen 0 und 2047 liegen.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| label                 |      |      |      |      |      | x    | x     | x    | x     |



 

Diese Anweisung definiert eine Bezeichnung, die sich in der nächsten shaderanweisung befindet. Die Bezeichnungs Anweisung kann nur direkt nach einer [ret](ret---ps.md) -Anweisung vorhanden sein (die das Ende der vorherigen Unterroutine oder des Hauptprogramms definiert).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




