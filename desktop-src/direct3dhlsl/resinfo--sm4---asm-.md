---
title: resinfo (sm4 – asm)
description: Fragen Sie die Dimensionen einer bestimmten Eingaberessource ab.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb23a6790c113702e59fc53f85a4d838907fe5ff658c29d83e37e3f620a9dc79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095320"
---
# <a name="resinfo-sm4---asm"></a>resinfo (sm4 – asm)

Fragen Sie die Dimensionen einer bestimmten Eingaberessource ab.



| resinfo \[ \_ uint\|\_rcpFloat \] dest \[ .mask \] , srcMipLevel.select \_ component, srcResource \[ .swizzle\] |
|-----------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/>                             |
| <span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*<br/> | \[in \] Die MIP-Ebene.<br/>                                                          |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] der Eingabetextur A t \# oder \# u, für die die Dimensionen abgefragt werden. <br/> |



 

## <a name="remarks"></a>Hinweise

*srcMipLevel* wird als ganzzahliger Skalar ohne Vorzeichen gelesen, sodass eine einzelne Komponentenauswahl für das Quellregister erforderlich ist, wenn es sich nicht um einen unmittelbaren Skalarwert handelt.

*dest empfängt* \[ Breite, Höhe, Tiefe oder Arraygröße, Total-mip-count, \] ausgewählt durch die Schreibmaske.

Die zurückgegebenen Werte für Breite, Höhe und Tiefe gelten für die mip-Ebene, die vom *srcMipLevel-Parameter* ausgewählt wird, und sind unabhängig von der Größe der Texeldaten in der Anzahl der Texel. Für Multisampleressourcen (texture2D \[ Array \] \# MS) werden Breite und Höhe auch in Texel zurückgegeben, nicht in Stichproben.

Die in *dest.w* zurückgegebene MIP-Gesamtanzahl ist vom *srcMipLevel-Parameter* nicht betroffen.

Bei UAVs \# (u) beträgt die Anzahl der Mip-Ebenen immer 1.

Alle Aspekte dieser Anweisung basieren auf den Merkmalen der Ressourcenansicht, die an t /u gebunden \# \# ist, nicht auf der zugrunde liegenden Basisressource.

Zurückgegebene Werte sind alle Gleitkommawerte, es sei denn, der \_ uint-Modifizierer wird verwendet. In diesem Fall handelt es sich bei den zurückgegebenen Werten um ganze Zahlen. Wenn der \_ rcpFloat-Modifizierer verwendet wird, sind alle zurückgegebenen Werte Gleitkommawerte, und Breite, Höhe und Tiefe werden als Reziproke zurückgegeben (1,0f/Breite, 1,0f/Höhe, 1,0f/Tiefe), einschließlich INF, wenn Breite/Höhe/Tiefe aus dem *srcMipLevel-Verhalten* außerhalb des Bereichs 0 sind. Der \_ rcpFloat-Modifizierer gilt nur für die zurückgegebenen Werte für Breite, Höhe und Tiefe und gilt nicht für Werte, die auf 0 festgelegt und somit nicht zurückgegeben werden, und gilt auch nicht für Rückgaben der Arraygröße.

Mit swizzle auf *srcResource* können die zurückgegebenen Werte willkürlich swizziert werden, bevor sie in das Ziel geschrieben werden.

Wenn *srcResource* eine Texture1D ist, wird die Breite in *dest.x* zurückgegeben, und *dest.yz* wird auf 0 festgelegt.

Wenn *srcResource* ein Texture1DArray ist, wird die Breite in *dest.x* zurückgegeben, die Arraygröße wird in *dest.y* zurückgegeben, und *dest.z* wird auf 0 festgelegt.

Wenn *srcResource* eine Texture2D ist, werden Breite und Höhe in *dest.xy* zurückgegeben, und *dest.z* wird auf 0 festgelegt.

Wenn *srcResource* ein Texture2DArray ist, werden Breite und Höhe in *dest.xy* zurückgegeben, und die Arraygröße wird in *dest.z* zurückgegeben.

Wenn *srcResource* eine Texture3D ist, werden Breite, Höhe und Tiefe in *dest.xyz* zurückgegeben.

Wenn *srcResource* ein TextureCube ist, werden die Breite und Höhe der einzelnen Cubegesichtsdimensionen in *dest.xy* zurückgegeben, und *dest.z* wird auf 0 festgelegt.

Wenn *srcResource* ein TextureCubeArray ist, werden die Breite und Höhe der einzelnen Cubegesichtsdimensionen in *dest.xy* zurückgegeben. *dest.z* ist auf einen nicht definierten Wert festgelegt.

Wenn die Mip-Klammer pro Ressource für *srcResource* angegeben wurde, gibt resinfo immer die Gesamtzahl der Mipmaps in der Ansicht für die Mip-Anzahl zurück, unabhängig von der Klammer. Wenn die Dimensionen eines bestimmten miplevels jedoch von resinfo angefordert werden und die miplevel abgesperrt wurden (z. B. bedeutet eine Klammer von 2,2, dass die Mips 0 und 1 gebunden wurden), sind die zurückgegebenen Dimensionen nicht definiert. Einige Implementierungen geben das verhalten außerhalb der Grenzen zurück, das für resinfo angegeben wird, wenn das miplevel außerhalb des Bereichs liegt. Andere Implementierungen geben die Abmessungen des Mip zurück, als ob sie nicht angeklammert worden wären.

### <a name="restrictions"></a>Beschränkungen

-   *srcResource* muss ein t- \# oder \# u-Register sein, das kein Puffer, sondern eine Textur \* ist.
-   Die relative Adressierung von *srcResource* ist nicht zulässig.
-   *srcMipLevel* muss eine einzelne Komponentenauswahl verwenden, wenn es sich nicht um einen skalaren unmittelbaren Selektor handelt.
-   Beim Abrufen von "t" \# oder \# "u", an das nichts gebunden ist, wird 0 für Breite, Höhe, Tiefe oder Arraygröße und gesamter MIP-Wert zurückgegeben. Der \_ rcpFloat-Modifizierer wird in diesem Fall weiterhin berücksichtigt, wodurch INF für die entsprechenden zurückgegebenen Werte zurückgegeben wird.
-   Wenn *srcMipLevel* außerhalb des Bereichs der verfügbaren Anzahl von miplevels in der Ressource liegt, ist das Verhalten für die Größenrückgabe (*dest.xyz*) mit dem Verhalten einer ungebundenen t- \# oder \# u-Ressource identisch. Die Gesamtanzahl der MIP-Daten wird in diesem Fall weiterhin in *dest.w* zurückgegeben.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

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

 

 





