---
title: Texturkoordinaten Register (HLSL PS-Referenz)
description: Ein Pixel-Shader-Eingabe Register, das Texturkoordinaten enthält.
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 456ea0da6c1c23f51dbdba357f18de747b318e6a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104976512"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a>Texturkoordinaten Register (HLSL PS-Referenz)

Ein Pixel-Shader-Eingabe Register, das Texturkoordinaten enthält.



| Pixel-Shader-Versionen       | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| Texturkoordinaten Register |      |      |      |      | x    | x     | x    | x    | x     |



 

Ein Texturkoordinaten Register enthält Texturkoordinaten Daten. Bevor ein Texturkoordinaten Register verwendet wird, muss es durch eine Pixel-Shader-Deklaration deklariert werden. Ausführliche Informationen zum Deklarieren eines Textur Registers finden Sie unter [DCL-(SM2, SM3-PS ASM)](dcl---ps.md).

Außerdem sind hier einige weitere Eigenschaften von Texturkoordinaten Registern aufgeführt.

-   Es gibt acht Pixel-Shader-Texturkoordinaten Register, t0 bis T7.
-   Hierbei handelt es sich um schreibgeschützte Register.
-   Sie enthalten vier Komponenten-RGBA-Werte, die aus Eingabe Scheitel Punkten durchlaufen werden.
-   Sie enthalten hohe Genauigkeit, hohe dynamische Bereichs Datenwerte, die von den Scheitelpunkt Daten interpoliert werden. Werte werden mit Perspective-korrekter interpolung generiert. Bei den Daten handelt es sich um Gleit Komma Genauigkeit und wird signiert.
-   Es gibt maximal einen in einer einzigen Anweisung.
-   Mehrere Lesevorgänge eines Texturkoordinaten Registers innerhalb eines Shaders müssen die identische [Schreib Maske für das Ziel Register](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)verwenden.
-   Die optionale PP für partielle Genauigkeits Modifizierer \[ \_ \] gilt für abhängige Lesevorgänge. Dies liegt daran, dass die Teil Genauigkeit die arithmetischen Operationen mit dem Texturkoordinaten Register beeinflusst. Sie wirkt sich nicht auf die Genauigkeit von Textur Adress Anweisungen aus, da Sie sich nicht auf die Iteratoren der Textur Koordinate auswirkt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




