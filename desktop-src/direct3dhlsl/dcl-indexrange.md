---
title: dcl_indexRange (sm4 – asm)
description: dcl \_ indexRange (sm4 – asm)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a652d200a211eb5528f6e7ecdedf2cc20579817d1f0148d59855d1e864de55de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727190"
---
# <a name="dcl_indexrange-sm4---asm"></a>dcl \_ indexRange (sm4 – asm)

Deklariert einen Bereich von Registern, auf die über den Index zugegriffen wird (eine ganze Zahl, die im Shader berechnet wird).



| dcl \_ indexRange *minRegisterM*, *maxRegisterN* |
|------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em><br/></td>
<td>[in] Das erste Register für den Zugriff nach Index. <br/>
<ul>
<li><em>minRegister</em> ist entweder <strong>v</strong> für ein Vertex- oder Pixel-Shader-Eingaberegister oder <strong>o</strong> für ein Vertex-Shader-Ausgaberegister.</li>
<li><em>M</em> ist eine ganze Zahl, die die Registernummer angibt.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em><br/></td>
<td>[in] Das letzte Register, auf das nach Index zugegriffen werden soll. Das gleiche Formular wie <em>minRegister</em> mit Ausnahme <em>von N</em> ist die Registernummer.<br/></td>
</tr>
</tbody>
</table>



 

Die folgenden Einschränkungen gelten für alle Register:

-   Die Register min und max müssen denselben Typ aufweisen und die gleichen Komponentenmasken aufweisen (wenn Masken deklariert werden).
-   Ein Register kann mehrere Indexbereiche aufweisen, solange sie sich nicht überschneiden.
-   Die Mindestregisternummer muss kleiner als die maximale Registernummer sein.
-   Ein Indexregister darf keinen [Systemwert](dx-graphics-hlsl-semantics.md)enthalten.
-   Das Indizieren eines Registers außerhalb der maximalen Indexdeklaration führt zu nicht definierten Ergebnissen.

Pixel-Shader-Eingaberegister müssen den gleichen Interpolationsmodus verwenden. Pixel-Shader-Ausgaberegister sind nicht indizierbar.

Ein Geometrie-Shader-Eingaberegister verfügt über zwei Dimensionen (Scheitelpunktachse, Attributachse); der Indexbereich gilt nur für die Attributachse, da die Scheitelpunktachse immer vollständig indizierbar ist.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Diese Anweisung ist enthalten, um das Debuggen eines Shaders in der Assembly zu unterstützen. Sie können keinen Shader in der Assemblysprache mit shader Model 4 erstellen.

## <a name="example"></a>Beispiel

Beispiel:


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



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

 

 





