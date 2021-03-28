---
title: sample_b (SM4-ASM)
description: Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus. | sample_b (SM4-ASM)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219323"
---
# <a name="sample_b-sm4---asm"></a>Beispiel \_ b (SM4-ASM)

Stichproben von Daten aus dem angegebenen Element/der Textur mithilfe der angegebenen Adresse und des vom angegebenen Sampler identifizierten Filter Modus.



| Sample \_ b \[ \_ aoffimmi (u, v, w) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler, srclodbias. Select- \_ Komponente |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse des Vorgangs Ergebnisses.<br/>                                                              |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>     | \[in \] einem Satz von Texturkoordinaten. Weitere Informationen finden Sie in der [Beispiel](sample--sm4---asm-.md) Anweisung.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] einem Textur Register. Weitere Informationen finden Sie in der **Beispiel** Anweisung.<br/>                                 |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*<br/>     | \[in \] einem Samplerregister. Weitere Informationen finden Sie in der **Beispiel** Anweisung.<br/>                                 |
| <span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srclodbias*<br/>     | \[\]Weitere Informationen zu diesem Parameter finden Sie im Abschnitt " **Hinweise** ".<br/>                                        |



 

## <a name="remarks"></a>Bemerkungen

Die Quelldaten können von jedem Ressourcentyp (außer Puffern) stammen. Im Rahmen der Anweisungs Ausführung wird eine zusätzliche Abweichung auf die Detailebene angewendet.

Diese Anweisung verhält sich wie die [Beispiel](sample--sm4---asm-.md) Anweisung mit dem Hinzufügen des angegebenen *srclodbias* -Werts auf den Detail Wert, der als Teil der Anweisungs Ausführung berechnet wurde, bevor die MIP-Karte ausgewählt wird. Der *srclodbias* -Wert wird der berechneten LOD auf Pixel Basis zusammen mit dem Sampler-miplodbias-Wert hinzugefügt, vor der Klammer an minlod und maxlod.

### <a name="restrictions"></a>Beschränkungen

-   **Beispiel \_ b** erbt dieselben Einschränkungen wie die [Beispiel](sample--sm4---asm-.md) Anweisung sowie zusätzliche Einschränkungen für den zusätzlichen Parameter.
-   Der Bereich von *srclodbias* ist (-16,0 f bis 15,99 f). Werte außerhalb dieses Bereichs führen zu undefinierten Ergebnissen.
-   *srclodbias* muss eine einzelne Komponentenauswahl verwenden, wenn es sich nicht um eine sofortige skalare handelt.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





