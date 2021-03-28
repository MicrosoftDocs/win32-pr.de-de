---
title: packoffset
description: 'Optionales Shader Constant Packaging-Schlüsselwort, das die folgende Syntax verwendet:'
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- packoffset HLSL
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6feeaa586abe30fa8a36c28d0298dc408cdfb099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312461"
---
# <a name="packoffset"></a>packoffset

Optionales Shader Constant Packaging-Schlüsselwort, das die folgende Syntax verwendet:



|                                                 |
|-------------------------------------------------|
| : packoffset (c- \[ Unterkomponente \] \[ . Component \] ) |



 

## <a name="parameters"></a>Parameter



| Element                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**<br/>                                                                                                  | Erforderliches Schlüsselwort.<br/>                                                                                                                         |
| <span id="c"></span><span id="C"></span>**scher**<br/>                                                                                                                             | Die Verpackung gilt nur für konstante Register (c). <br/>                                                                                          |
| <span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent \] \[ . Component\]**<br/> | Optionale unter Komponenten und Komponenten. Eine Unterkomponente ist eine Registernummer, bei der es sich um eine ganze Zahl handelt. Eine Komponente hat die Form " \[ . xyzw" \] .<br/> |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Schlüsselwort, um beim [Deklarieren eines Variablen Typs](dx-graphics-hlsl-variable-syntax.md)eine shaderkonstante manuell zu verpacken.

Beim Verpacken einer Konstanten können keine Konstanten Typen gemischt werden.

Der Compiler verhält sich bei globalen Konstanten und einheitlichen Konstanten etwas anders:

-   Eine globale Konstante. Eine globale Variable wird einem *$Global* cBuffer vom Compiler als globale Konstante hinzugefügt. Automatisch gepackte Elemente (die ohne packoffset deklariert werden) werden nach der letzten manuell gepackten Variable angezeigt. Beim Packen von globalen Konstanten können Typen gemischt werden.
-   Eine einheitliche Konstante. Ein einheitlicher Parameter in der Parameterliste einer Funktion wird dem *$param* Konstanten Puffer vom Compiler hinzugefügt, wenn der Shader außerhalb des Effects-Frameworks kompiliert wird. Bei der Kompilierung innerhalb des Effect-Frameworks muss eine einheitliche Konstante in eine im globalen Gültigkeitsbereich definierte einheitliche Variable aufgelöst werden. Eine einheitliche Konstante kann nicht manuell versetzt werden. die empfohlene Verwendung ist nur für die Spezialisierung von Shadern, bei denen Sie an globale Daten zurückgegeben werden, nicht als Mittel zum Übergeben von Anwendungsdaten an den Shader.

Hier sind einige zusätzliche Beispiele: [Verpacken von Konstanten mithilfe von Shadermodell 4](dx-graphics-hlsl-packing-rules.md).

## <a name="examples"></a>Beispiele

Im folgenden finden Sie einige Beispiele für das manuelle Packen von shaderkonstanten.

Pack-unter Komponenten von Vektoren und skalaren, deren Größe groß genug ist, um das Überschreiten von Registrierungs Grenzen zu verhindern. Diese sind z. b. gültig:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Variablensyntax](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variablen (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





