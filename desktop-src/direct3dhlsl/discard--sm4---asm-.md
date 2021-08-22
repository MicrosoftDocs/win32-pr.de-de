---
title: discard (sm4 - asm)
description: Kennzeichnen Sie die Ergebnisse von Pixel Shader bedingt, die verworfen werden sollen, wenn das Programmende erreicht ist.
ms.assetid: 566C4A9A-B32A-4AA6-A888-70F6965B1B5A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6b5744ee8cf8d2953247711d95fe5d5ec6f96c36c700e1a38ce4e0cb1e1ff5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986600"
---
# <a name="discard-sm4---asm"></a>discard (sm4 - asm)

Kennzeichnen Sie die Ergebnisse von Pixel Shader bedingt, die verworfen werden sollen, wenn das Programmende erreicht ist.



| discard{ \_ z\|\_nz} src0.select-Komponente \_ |
|-------------------------------------------|



 



| Element                                                            | Beschreibung                                                                                       |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Der Wert, der bestimmt, ob das aktuelle Pixel, das verarbeitet wird, verworfen werden soll.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung kennzeichnet das aktuelle Pixel als beendet, während die Ausführung fortgesetzt wird, sodass andere Parallelausführungspixel bei Bedarf Ableitungen erhalten können. Obwohl die Ausführung fortgesetzt wird, werden alle Pixel Shader-Ausgabe-Schreibvorgänge vor oder nach der **Verwerfungsanweisung** verworfen.

Wenn für **discard \_ z** alle Bits in *der \_ src0.select-Komponente 0* (null) sind, wird das Pixel verworfen.

Wenn für **discard \_ nz** Bits in *der \_ src0.select-Komponente* ungleich 0 (null) sind, wird das Pixel verworfen.

Darüber hinaus kann die **Discard-Anweisung** in jedem Flusssteuerungskonstrukt vorhanden sein.

Mehrere **Verwerfungsanweisungen** können in einem Shader vorhanden sein, und wenn ein Shader ausgeführt wird, wird das Pixel beendet.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





