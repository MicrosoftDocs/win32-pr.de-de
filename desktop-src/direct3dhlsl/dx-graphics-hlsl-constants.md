---
title: Shaderkonstanten (HLSL)
description: In ShaderModell 4 werden Shaderkonst constants in mindestens einer Pufferressourcen im Arbeitsspeicher gespeichert.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- konstanter Puffer
- Texturpuffer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f314be4b8da98ff80bd7404c270479855e13fb6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129959"
---
# <a name="shader-constants-hlsl"></a>Shaderkonstanten (HLSL)

In ShaderModell 4 werden Shaderkonst constants in mindestens einer Pufferressourcen im Arbeitsspeicher gespeichert. Sie können in zwei Arten von Puffern organisiert werden: Konstante Puffer (Cbuffer) und Texturpuffer (Tbuffer). Konstante Puffer sind für die Verwendung konstanter Variablen optimiert, was sich durch den Zugriff mit geringerer Latenz und eine häufigere Aktualisierung der CPU ausdingt. Aus diesem Grund gelten zusätzliche Größen-, Layout- und Zugriffseinschränkungen für diese Ressourcen. Der Zugriff auf Texturpuffer erfolgt wie Texturen und verbessert die Leistung für beliebig indizierte Daten. Unabhängig davon, welche Art von Ressource Sie verwenden, gibt es keine Beschränkung für die Anzahl konstanter Puffer oder Texturpuffer, die eine Anwendung erstellen kann.

Das Deklarieren eines konstanten Puffers oder Texturpuffers sieht sehr ähnlich wie eine Strukturdeklaration in C aus, mit dem Hinzufügen der Schlüsselwörter **register** und **packoffset** zum manuellen Zuweisen von Registern oder Packen von Daten.



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| *BufferType* \[ *Name* \] \[: **register**(b \# ) { \] *VariableDeclaration* \[ : **packoffset**(c \# .xyzw) \] ;      ... }; |



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*
</dt> <dd>

\[in \] Der Puffertyp.



| BufferType | Beschreibung     |
|------------|-----------------|
| cbuffer    | konstanter Puffer |
| tbuffer    | Texturpuffer  |



 

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Namen*
</dt> <dd>

\[in \] Optional, ASCII-Zeichenfolge, die einen eindeutigen Puffernamen enthält.

</dd> <dt>

<span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b \# )
</dt> <dd>

\[im \] Optional-Schlüsselwort, das zum manuellen Packen konstanter Daten verwendet wird. Konstanten können in einem Register nur in einem konstanten Puffer gepackt werden, wobei das Startregister durch die Registernummer ( ) angegeben *\#* wird.

</dd> <dt>

<span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*
</dt> <dd>

\[in \] Variable-Deklaration, ähnlich einer Struktur-Memberdeklaration. Dies kann ein beliebiger HLSL-Typ oder ein Effektobjekt sein (mit Ausnahme einer Textur oder eines Samplerobjekts).

</dd> <dt>

<span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# .xyzw)
</dt> <dd>

\[im \] Optional-Schlüsselwort, das zum manuellen Packen konstanter Daten verwendet wird. Konstanten können in einem beliebigen konstanten Puffer gepackt werden, wobei die Registernummer durch ( ) angegeben *\#* wird. Das Packen von Unterkomponenten (mit xyzw swizzling) ist für Konstanten verfügbar, deren Größe in ein einzelnes Register passt (nicht über eine Registergrenze hinaus). Beispielsweise konnte ein float4-Element nicht in ein einzelnes Register gepackt werden, das mit der y-Komponente beginnt, da es nicht in ein Vier-Komponenten-Register passen würde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Konstante Puffer verringern die Bandbreite, die zum Aktualisieren von Shaderkonstten erforderlich ist, indem shader-Konstanten gleichzeitig gruppiert und ein Commit für diese konstanten Konstanten ermöglicht wird, anstatt einzelne Aufrufe zum getrennten Commit jeder Konstante zu tätigen.

Ein konstanter Puffer ist eine spezialisierte Pufferressource, auf die wie ein Puffer zugegriffen wird. Jeder konstante Puffer kann bis zu 4.096 [Vektoren halten.](dx-graphics-hlsl-vector.md) Jeder Vektor enthält bis zu vier 32-Bit-Werte. Sie können bis zu 14 konstante Puffer pro Pipelinephase binden (zwei zusätzliche Slots sind für die interne Verwendung reserviert).

Ein Texturpuffer ist eine spezialisierte Pufferressource, auf die wie eine Textur zugegriffen wird. Der Texturzugriff (im Vergleich zum Pufferzugriff) kann eine bessere Leistung für beliebig indizierte Daten aufweisen. Sie können bis zu 128 Texturpuffer pro Pipelinephase binden.

Eine Pufferressource ist so konzipiert, dass der Mehraufwand für das Festlegen von Shaderkonst constants minimiert wird. Das Effektframework (siehe [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) verwaltet aktualisierungskonstierte und Texturpuffer, oder Sie können die Direct3D-API verwenden, um Puffer zu aktualisieren (weitere Informationen finden Sie unter Kopieren und Zugreifen auf Ressourcendaten [(Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) Eine Anwendung kann auch Daten aus einem anderen Puffer (z. B. einem Renderziel oder einem Streamausgabeziel) in einen konstanten Puffer kopieren.

Weitere Informationen zur Verwendung konstanter Puffer in einer D3D10-Anwendung finden Sie unter [Ressourcentypen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) und Erstellen von Pufferressourcen [(Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating)

Weitere Informationen zur Verwendung konstanter Puffer in einer D3D11-Anwendung finden Sie unter [Introduction to Buffers in Direct3D 11 (Einführung in Puffer in Direct3D 11)](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) und [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)(Erstellen eines konstanten Puffers).

Ein konstanter Puffer erfordert nicht, [dass eine](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) Sicht an die Pipeline gebunden ist. Ein Texturpuffer erfordert jedoch eine Ansicht und muss an einen Texturslot gebunden sein (oder bei Verwendung eines Effekts an [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) gebunden sein).

Es gibt zwei Möglichkeiten, Konstantendaten zu packen: die Schlüsselwörter [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) und [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)

Unterschiede zwischen Direct3D 9 und Direct3D 10 und 11:

- Im Gegensatz zur automatischen Zuordnung von Konstanten in Direct3D 9, die keine Packung durchführen und stattdessen jede Variable einem Satz von float4-Registern zugewiesen haben, folgen HLSL-Konstantenvariablen den Füllregeln in Direct3D 10 und 11.



 

### <a name="organizing-constant-buffers"></a>Organisieren konstanter Puffer

Konstante Puffer verringern die Bandbreite, die zum Aktualisieren von Shaderkonstten erforderlich ist, indem shader-Konstanten gleichzeitig gruppiert und ein Commit für diese konstanten Konstanten ermöglicht wird, anstatt einzelne Aufrufe zum getrennten Commit jeder Konstante zu tätigen.

Die beste Möglichkeit zur effizienten Nutzung von Konstantenpuffern ist die Organisation von Shadervariablen in Konstantenpuffern anhand der Updatehäufigkeit. Dadurch kann eine Anwendung die bandbreite minimieren, die zum Aktualisieren von Shaderkonst constants erforderlich ist. Beispielsweise kann ein Shader zwei konstante Puffer deklarieren und die Daten in jedem basierend auf der Aktualisierungshäufigkeit organisieren: Daten, die pro Objekt aktualisiert werden müssen (z. B. eine Weltmatrix), werden in einem konstanten Puffer gruppiert, der für jedes Objekt aktualisiert werden kann. Dies ist getrennt von Daten, die eine Szene charakterisieren, und wird daher wahrscheinlich viel seltener aktualisiert (wenn sich die Szene ändert).


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a>Standardkonst constant buffers (Standardkonst constant buffers)

Es sind zwei Standardkonst constant-Puffer verfügbar: $Global und $Param. Variablen, die im globalen Bereich platziert werden, werden dem $Global cbuffer implizit hinzugefügt. Dabei wird die gleiche Füllmethode verwendet, die auch für cbuffers verwendet wird. Einheitliche Parameter in der Parameterliste einer Funktion werden im $Param angezeigt, wenn ein Shader außerhalb des Effektframework kompiliert wird. Bei der Kompilierung innerhalb des Effektframework müssen alle Uniformen in Variablen auflösen, die im globalen Gültigkeitsbereich definiert sind.

## <a name="examples"></a>Beispiele

Hier sehen Sie ein Beispiel aus [dem Skinning10-Beispiel,](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) bei dem es sich um einen Texturpuffer handelt, der aus einem Array von Matrizen besteht.


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



Diese Beispieldeklaration weist manuell einen konstanten Puffer zu, um bei einem bestimmten Register zu beginnen, und packt auch bestimmte Elemente nach Unterkomponenten.


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

