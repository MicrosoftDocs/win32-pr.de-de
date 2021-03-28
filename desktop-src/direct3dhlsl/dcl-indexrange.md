---
title: dcl_indexRange (SM4-ASM)
description: DCL \_ -indexrange (SM4-ASM)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b0e2c250afd4ce52729a4c4bffeee0f33e4be6b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976497"
---
# <a name="dcl_indexrange-sm4---asm"></a>DCL \_ -indexrange (SM4-ASM)

Deklariert einen Bereich von Registern, auf die über den Index zugegriffen wird (eine im Shader berechnete Ganzzahl).



| DCL \_ indexrange *minregisterm*, *maxRegisterN* |
|------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minregisterm</em><br/></td>
<td>in Das erste Register für den Zugriff nach Index. <br/>
<ul>
<li><em>minregister</em> ist entweder <strong>v</strong> für ein Vertex-oder Pixel-Shader-Eingabe Register oder <strong>o</strong> für ein Vertex-Shader-Ausgabe Register.</li>
<li><em>M</em> ist eine ganze Zahl, die die Registernummer bezeichnet.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em><br/></td>
<td>in Das letzte Register für den Zugriff nach Index. Dieselbe Form wie " <em>minregister</em> " mit Ausnahme von " <em>N</em> " ist die Registernummer.<br/></td>
</tr>
</tbody>
</table>



 

Die folgenden Einschränkungen gelten für alle Register:

-   Die min-und Max-Register müssen denselben Typ aufweisen und dieselben Komponenten Masken aufweisen (Wenn Masken deklariert sind).
-   Ein Register kann mehrere Index Bereiche enthalten, solange Sie sich nicht überlappen.
-   Die minimale Registernummer muss kleiner als die maximale Registernummer sein.
-   Ein Indexregister darf keinen [System Wert](dx-graphics-hlsl-semantics.md)enthalten.
-   Die Indizierung eines Registers außerhalb der maximalen Index Deklaration erzeugt nicht definierte Ergebnisse.

Pixel-Shader-Eingabe Register müssen denselben Interpolations Modus verwenden. Pixel-Shader-Ausgabe Register können nicht indiziert werden.

Ein Geometrie-Shader-Eingabe Register hat zwei Dimensionen (vertexachse, Attribut Achse); der Index Bereich gilt nur für die Attribut Achse, da die vertexachse immer vollständig indizierbar ist.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Es ist nicht möglich, einen Shader mit Shadermodell 4 in der Assemblysprache zu erstellen.

## <a name="example"></a>Beispiel

Beispiel:


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



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

 

 





