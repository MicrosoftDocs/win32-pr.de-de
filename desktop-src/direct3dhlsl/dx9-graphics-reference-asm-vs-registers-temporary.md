---
title: Temporäres Register (HLSL vs-Referenz)
description: Ein temporäres Vertex-Shader-Register wird verwendet, um Zwischenergebnisse zu speichern.
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313799"
---
# <a name="temporary-register-hlsl-vs-reference"></a>Temporäres Register (HLSL vs-Referenz)

Ein temporäres Vertex-Shader-Register wird verwendet, um Zwischenergebnisse zu speichern.

Ein temporäres Register muss initialisiert werden, bevor es verwendet wird. Jedes temporäre Register verfügt über einen einzelschreibzugriff und einen dreifach Lesezugriff. Dies bedeutet, dass eine einzelne Shader-Anweisung bis zu drei temporäre Register als Eingaben verwenden kann.

Werte in einem temporären Register, die aus vorangehenden Aufrufen des Vertex-Shaders verbleiben, können nicht verwendet werden.

Ein Register besteht aus Eigenschaften, die bestimmen, wie sich die einzelnen Register Verhalten.



| Eigenschaft        | BESCHREIBUNG                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name            | r \[ n \] . n ist eine optionale Registernummer. Der Standardwert ist 0, und ist der Wert, der verwendet wird, wenn kein Wert angegeben wird.                                                                                 |
| Anzahl           | Maximal 12 Register.                                                                                                                                                                  |
| E/a-Berechtigungen | Lese-/Schreibzugriff. Dieses Register kann von der API oder vom Shader gelesen oder geschrieben werden.                                                                                                               |
| Leseports      | Die Häufigkeit, mit der ein Register innerhalb einer einzigen Anweisung gelesen werden kann, ist 3. Ein temporäres Register ist das einzige Register, das mehr als einmal in einer einzigen Anweisung gelesen und geschrieben werden kann. |



 

Jedes temporäre Register verfügt über einen einzelschreibzugriff und einen dreifach Lesezugriff. Aus diesem Grund kann eine Anweisung in der Gruppe der Eingabe Quell Operanden bis zu drei temporäre Register aufweisen.

Es können keine Werte in einem temporären Register verwendet werden, die aus vorangehenden Aufrufen des Vertex-Shaders verbleiben. Vertex-Shader, die vor dem Schreiben einen Wert aus einem temporären Register lesen, führen zum Erstellen des Vertexshaders nicht zum Direct3D-API-aufrufen.

## <a name="example"></a>Beispiel

Im folgenden finden Sie ein Beispiel für die Verwendung eines temporären Registers:


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Temporäres Register     | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




