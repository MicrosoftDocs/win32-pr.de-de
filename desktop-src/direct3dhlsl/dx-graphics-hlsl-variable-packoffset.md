---
title: packoffset
description: Optionales Shader-Schlüsselwort für konstantes Packen, das die folgende Syntax verwendet
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
ms.openlocfilehash: 5c92a6375f0724a1910fc0f09b47e1593614f9f1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826079"
---
# <a name="packoffset"></a>packoffset

Optionales Shader-Schlüsselwort für konstantes Packen, das die folgende Syntax verwendet:

: packoffset( c \[ Subcomponent \] \[ .component \] )



 

## <a name="parameters"></a>Parameter



| Element                                                                                                                                                                                 | Beschreibung                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**<br/>                                                                                                  | Erforderliches Schlüsselwort.<br/>                                                                                                                         |
| <span id="c"></span><span id="C"></span>**C**<br/>                                                                                                                             | Das Packen gilt nur für konstante Register (c). <br/>                                                                                          |
| <span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Komponente der \] \[ Unterkomponente\]**<br/> | Optionale Unterkomponenten und Komponenten. Eine Unterkomponenten ist eine Registernummer, die eine ganze Zahl ist. Eine Komponente hat die Form \[ .xyzw \] .<br/> |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Schlüsselwort, um beim Deklarieren eines Variablentyps manuell eine [Shaderkonstance zu packen.](dx-graphics-hlsl-variable-syntax.md)

Beim Packen einer Konstante können Sie keine konstanten Typen mischen.

Der Compiler verhält sich für globale Konstanten und einheitliche Konstanten etwas anders:

-   Eine globale Konstante. Eine globale Variable wird als globale Konstante zu einem $Global *vom* Compiler hinzugefügt. Automatisch gepackte Elemente (die ohne packoffset deklariert sind) werden nach der zuletzt manuell gepackten Variablen angezeigt. Sie können Typen beim Packen globaler Konstanten mischen.
-   Eine einheitliche Konstante. Ein einheitlicher Parameter in der Parameterliste einer Funktion wird einem *$Param* konstanten Puffer vom Compiler hinzugefügt, wenn der Shader außerhalb des Effektframework kompiliert wird. Bei der Kompilierung innerhalb des Effektframework muss eine einheitliche Konstante in eine im globalen Gültigkeitsbereich definierte einheitliche Variable auflösen. Eine einheitliche Konstante kann nicht manuell versetzt werden. ihre empfohlenen Verwendung ist nur für die Spezialisierung von Shadern, bei denen sie einen Alias zurück zu globalen Namen erstellen, und nicht als Mittel zur Übergabe von Anwendungsdaten an den Shader.

Im Folgenden finden Sie einige zusätzliche Beispiele: [Packen von Konstanten mithilfe des Shadermodells 4](dx-graphics-hlsl-packing-rules.md).

## <a name="examples"></a>Beispiele

Im Folgenden finden Sie einige Beispiele für das manuelle Packen von Shaderkonst constants.

Packen Sie Unterkomponenten von Vektoren und Skalaren, deren Größe groß genug ist, um das Überschreiten von Registergrenzen zu verhindern. Dies sind beispielsweise alle gültig:


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Variablensyntax](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variablen (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





