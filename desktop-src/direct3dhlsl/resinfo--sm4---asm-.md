---
title: ResInfo (SM4-ASM)
description: Abfragen der Dimensionen einer bestimmten Eingabe Ressource.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a252195a4b59ed791f6ac625fe1d95bbd9925f1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389523"
---
# <a name="resinfo-sm4---asm"></a>ResInfo (SM4-ASM)

Abfragen der Dimensionen einer bestimmten Eingabe Ressource.



| ResInfo \[ \_ uint \|\_rcpfloat \] dest \[ . mask \] , srcmiplevel. Select \_ Component, srkresource \[ . Swizzle\] |
|-----------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse des Vorgangs Ergebnisses.<br/>                             |
| <span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcmiplevel*<br/> | \[auf \] der MIP-Ebene.<br/>                                                          |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] einer t- \# oder u- \# Eingabe Textur, für die die Dimensionen abgefragt werden. <br/> |



 

## <a name="remarks"></a>Bemerkungen

*srcmiplevel* wird als ganzzahliger Skalarwert ohne Vorzeichen gelesen, sodass eine einzelne Komponentenauswahl für das Quell Register erforderlich ist, wenn es sich nicht um einen skalaren unmittelbaren Wert handelt.

*dest* empfängt \[ Breite, Höhe, Tiefe oder Array Größe, gesamter MIP-Count \] , von der Schreib Maske ausgewählt.

Die zurückgegebenen Werte für Breite, Höhe und Tiefe gelten für die durch den *srcmiplevel* -Parameter ausgewählte MIP-Ebene und sind unabhängig von der texgrößengröße in der Anzahl von texeln. Bei Multisampling-Ressourcen (texture2D \[ array \] MS \# ) werden Breite und Höhe auch in Texels und nicht in Beispielen zurückgegeben.

Der *srcmiplevel* -Parameter hat keine Auswirkungen auf die Gesamtanzahl der in *dest. w* zurückgegebenen MIP-Anzahl.

Bei UAVs (u \# ) ist die Anzahl der MIP-Ebenen immer 1.

Alle Aspekte dieser Anweisung basieren auf den Merkmalen der Ressourcen Sicht, die an t \# /u gebunden \# ist, nicht an der zugrunde liegenden Basis Ressource.

Zurückgegebene Werte sind alle Gleit Komma Werte, es sei denn \_ , der uint-Modifizierer wird verwendet. in diesem Fall sind die zurückgegebenen Werte alle Ganzzahlen. Wenn der \_ rcpfloat-Modifizierer verwendet wird, sind alle zurückgegebenen Werte Gleit Komma Werte, und die Breite, Höhe und Tiefe werden als Gegenstücke (1.0 f/Width, 1.0 f/Height, 1.0 f/Tiefe) zurückgegeben, einschließlich inf, wenn "width/height/Tiefe" den Wert "0" für das außerhalb des gültigen *srcmiplevel* Der \_ rcpfloat-Modifizierer gilt nur für Werte vom Typ "width", "Height" und "Tiefe" und gilt nicht für Werte, die auf "0" festgelegt sind und daher nicht zurückgegeben werden, und gilt nicht für die Rückgabe von Array Größen.

Das Swizzle in *srkresource* ermöglicht es, dass die zurückgegebenen Werte willkürlich durchlaufen werden, bevor Sie in das Ziel geschrieben werden.

Wenn *srkresource* ein Texture1D ist, wird Width in *dest. x* zurückgegeben, und *dest. YZ* wird auf 0 festgelegt.

Wenn *srkresource* ein Texture1DArray ist, wird "width" in " *dest. x*" zurückgegeben, die Array Größe wird in " *dest. y*" zurückgegeben, und " *dest. z* " wird auf 0 festgelegt.

Wenn *srkresource* ein Texture2D-Wert ist, werden Width und height in " *dest. XY*" zurückgegeben, und " *dest. z* " wird auf 0 festgelegt.

Wenn *srkresource* ein Texture2DArray ist, werden Width und height in " *dest. XY*" zurückgegeben, und die Array Größe wird in " *dest. z*" zurückgegeben.

Wenn *srkresource* ein Texture3D-Wert ist, werden Width, Height und Tiefe in *dest.XYZ* zurückgegeben.

Wenn *srkresource* ein texturecube-Element ist, werden die Breite und Höhe der einzelnen Dimensions Abmessungen in " *dest. XY*" zurückgegeben, und " *dest. z* " wird auf 0 festgelegt.

Wenn *srkresource* ein texturecubearray ist, werden die Dimensionen Breite und Höhe in den Dimensionen " *dest. XY*" zurückgegeben. " *dest. z* " ist auf einen nicht definierten Wert festgelegt.

Wenn für *srkresource* die MIP-Klammer pro Ressource angegeben wurde, gibt ResInfo unabhängig von der Klammer immer die Gesamtzahl von Mipmaps in der Ansicht für die MIP-Anzahl zurück. Wenn jedoch die Dimensionen einer bestimmten miplevel von ResInfo angefordert werden und die miplevel-Methode ausgeschaltet wurde (z. b. eine Klammer von 2,2 bedeutet, dass MIPS 0 und 1 geklemmt wurden), sind die zurückgegebenen Dimensionen nicht definiert. Einige Implementierungen geben das Verhalten von außerhalb des gültigen Bereichs für ResInfo zurück, wenn sich die miplevel außerhalb des gültigen Bereichs befindet. Andere Implementierungen geben die Dimensionen des MIP so zurück, als würden Sie nicht geklammert werden.

### <a name="restrictions"></a>Beschränkungen

-   *srkresource* muss ein t- \# oder u-Register sein, \# das kein Puffer ist, sondern eine Textur ist \* .
-   Die relative Adressierung von *srkresource* ist nicht zulässig.
-   *srcmiplevel* muss eine einzelne Komponentenauswahl verwenden, wenn es sich nicht um eine sofortige skalare handelt.
-   Durch das Abrufen von t \# oder u \# , das nichts daran gebunden ist, wird 0 für Breite, Höhe, Tiefe oder arraySize und "Total-MIP-count" zurückgegeben. Der \_ rcpfloat-Modifizierer wird in diesem Fall immer noch berücksichtigt und gibt daher inf für die anwendbaren zurückgegebenen Werte zurück.
-   Wenn *srcmiplevel* außerhalb des Bereichs der verfügbaren Anzahl von miplevels in der Ressource liegt, ist das Verhalten der Größen Rückgabe (*dest.XYZ*) identisch mit der einer ungebundenen t- \# oder u- \# Ressource. Die gesamte MIP-Anzahl wird in diesem Fall weiterhin in " *dest. w* " zurückgegeben.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





