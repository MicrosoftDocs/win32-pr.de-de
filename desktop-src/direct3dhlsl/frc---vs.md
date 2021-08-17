---
title: frc – vs
description: Gibt den Bruchteil jeder Eingabekomponente zurück. | frc – vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2ecc6a1c903f78fb7c03442809f792e3ddb984d04975d3f5ecb0b5c918f7ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117907643"
---
# <a name="frc---vs"></a>frc – vs

Gibt den Bruchteil jeder Eingabekomponente zurück.

## <a name="syntax"></a>Syntax



| frc dst, src |
|--------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Frc                    | x    | x    | x    | x     | x    | x     |



 

Das folgende Codefragment zeigt konzeptionell, wie die Anweisung funktioniert.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



Die floor-Funktion konvertiert das übergebene Argument in die größte ganze Zahl, die kleiner als (oder gleich) dem Argument ist. Dies wird in einen float-Wert konvertiert und dann für den ursprünglichen Wert subtrahiert. Der resultierende Bruchwert liegt zwischen 0,0 und 1,0.

Für Version 1 \_ 1 sind die zulässigen Schreibmasken .y und .xy (.x ist nicht zulässig).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




