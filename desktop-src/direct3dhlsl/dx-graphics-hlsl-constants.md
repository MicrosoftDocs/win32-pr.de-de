---
title: Shaderkonstanten (HLSL)
description: In Shader Model 4 werden Shader-Konstanten in mindestens einer Puffer Ressource im Arbeitsspeicher gespeichert.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cBuffer
- tBuffer
- konstanter Puffer
- Textur Puffer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1b78da747a248bf4bb5774add1bf97f14f048c4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739432"
---
# <a name="shader-constants-hlsl"></a>Shaderkonstanten (HLSL)

In Shader Model 4 werden Shader-Konstanten in mindestens einer Puffer Ressource im Arbeitsspeicher gespeichert. Sie können in zwei Puffer Typen organisiert werden: Konstante Puffer (cbuffers) und Textur Puffer (tbuffers). Konstante Puffer sind für die Verwendung konstanter Variablen optimiert, die durch den Zugriff auf geringere Latenz und häufigere Updates von der CPU gekennzeichnet ist. Aus diesem Grund gelten für diese Ressourcen zusätzliche Größen-, Layout-und Zugriffsbeschränkungen. Textur Puffer werden wie Texturen aufgerufen und erzielen bei beliebig indizierten Daten eine bessere Leistung. Unabhängig davon, welchen Ressourcentyp Sie verwenden, gibt es keine Beschränkung für die Anzahl der Konstanten Puffer oder Textur Puffer, die eine Anwendung erstellen kann.

Das Deklarieren eines konstanten Puffers oder eines Textur Puffers ähnelt einer Struktur Deklaration in C, mit dem Hinzufügen der Schlüsselwörter " **Register** " und " **packoffset** " zum manuellen Zuweisen von Registern oder Packen von Daten.



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| *Buffertype* \[ *Name* \] \[: **Register**(b \# ) \] { *variabledeclaration* \[ : **packoffset**(c \# . xyzw) \] ;      ... }; |



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*Buffertype*
</dt> <dd>

\[im \] Puffertyp.



| Buffertype | BESCHREIBUNG     |
|------------|-----------------|
| cBuffer    | konstanter Puffer |
| tBuffer    | Textur Puffer  |



 

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*
</dt> <dd>

\[in \] Optionaler ASCII-Zeichenfolge, die einen eindeutigen Puffer Namen enthält.

</dd> <dt>

<span id="register_b__"></span><span id="REGISTER_B__"></span>**registrieren**(b \# )
</dt> <dd>

\[im \] optionalen Schlüsselwort wird verwendet, um konstante Daten manuell zu verpacken. Konstanten können nur in einem konstanten Puffer in ein Register gepackt werden, wobei das Start Register von der Registernummer () angegeben wird *\#* .

</dd> <dt>

<span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*Variabledeclaration*
</dt> <dd>

\[in der \] Variablen Deklaration, ähnlich wie eine Strukturmember-Deklaration. Dabei kann es sich um einen beliebigen HLSL-Typ oder ein Effekt Objekt handeln (mit Ausnahme einer Textur oder eines samplerobjekts)

</dd> <dt>

<span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# . xyzw)
</dt> <dd>

\[im \] optionalen Schlüsselwort wird verwendet, um konstante Daten manuell zu verpacken. Konstanten können in jedem Konstanten Puffer verpackt werden, wobei die Registernummer durch () angegeben wird *\#* . Das Komprimieren von unter Komponenten (unter Verwendung von xyzw swizzling) ist für Konstanten verfügbar, deren Größe in ein einzelnes Register passt (keine Register Grenze überschreiten). Beispielsweise konnte ein float4 nicht in einem einzelnen Register gepackt werden, beginnend mit der y-Komponente, da es nicht in ein vier-Komponenten-Register passt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Konstantenpuffer reduzieren die erforderliche Bandbreite, um shaderkonstanten zu aktualisieren, indem Sie zulassen, dass Shader-Konstanten gleichzeitig gruppiert und ein Commit ausgeführt werden, anstatt einzelne Aufrufe zum separaten Commit der einzelnen Konstanten zu erstellen.

Ein konstanter Puffer ist eine spezialisierte Puffer Ressource, auf die wie ein Puffer zugegriffen wird. Jeder Konstante Puffer kann bis zu 4096 [Vektoren](dx-graphics-hlsl-vector.md)enthalten. Jeder Vektor enthält bis zu 4 32-Bit-Werte. Sie können bis zu 14 Konstante Puffer pro Pipeline-Stufe binden (2 zusätzliche Slots sind für die interne Verwendung reserviert).

Ein Textur Puffer ist eine spezialisierte Puffer Ressource, auf die wie eine Textur zugegriffen wird. Der Textur Zugriff (im Vergleich zum Puffer Zugriff) kann bei beliebig indizierten Daten eine bessere Leistung aufweisen. Sie können bis zu 128 Textur Puffer pro Pipeline-Phase binden.

Eine Puffer Ressource ist so konzipiert, dass der Aufwand für das Festlegen von shaderkonstanten minimiert wird. Das Effect-Framework (siehe [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) verwaltet das Aktualisieren von Konstanten und Textur Puffern, oder Sie können die Direct3D-API verwenden, um Puffer zu aktualisieren (Weitere Informationen finden Sie unter [Kopieren und Zugreifen auf Ressourcen Daten (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) ). Eine Anwendung kann auch Daten aus einem anderen Puffer (z. b. einem Renderziel oder einem streamausgabeziel) in einen konstanten Puffer kopieren.

Weitere Informationen zur Verwendung konstanter Puffer in einer d3d10-Anwendung finden Sie unter [Ressourcentypen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) und [Erstellen von Puffer Ressourcen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).

Informationen zur Verwendung konstanter Puffer in einer D3D11-Anwendung finden Sie unter [Einführung in Puffer in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) und Gewusst [wie: Erstellen eines konstanten Puffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).

Für einen konstanten Puffer ist es nicht erforderlich, dass eine [Ansicht](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) an die Pipeline gebunden wird. Ein Textur Puffer erfordert jedoch eine Sicht, die an einen Textur Slot gebunden werden muss (oder bei Verwendung eines Effekts mit [**settexturebuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) gebunden werden muss).

Es gibt zwei Möglichkeiten, Konstanten Daten zu verpacken: mithilfe der Schlüsselwörter [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) und [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .



|                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10 und 11:<br/> Anders als bei der automatischen Zuordnung von Konstanten in Direct3D 9, die keine Komprimierung durchgeführt und stattdessen jede Variable einem Satz von float4 Registern zugewiesen haben, folgen die HLSL-Konstanten Variablen den Verpackungs Regeln in Direct3D 10 und 11.<br/> |



 

### <a name="organizing-constant-buffers"></a>Organisieren konstanter Puffer

Konstantenpuffer reduzieren die erforderliche Bandbreite, um shaderkonstanten zu aktualisieren, indem Sie zulassen, dass Shader-Konstanten gleichzeitig gruppiert und ein Commit ausgeführt werden, anstatt einzelne Aufrufe zum separaten Commit der einzelnen Konstanten zu erstellen.

Die beste Möglichkeit zur effizienten Nutzung von Konstantenpuffern ist die Organisation von Shadervariablen in Konstantenpuffern anhand der Updatehäufigkeit. Dadurch kann eine Anwendung die erforderliche Bandbreite zum Aktualisieren von shaderkonstanten minimieren. Ein Shader kann z. b. zwei Konstante Puffer deklarieren und die Daten auf der Grundlage ihrer Aktualisierungshäufigkeit organisieren: Daten, die pro Objekt aktualisiert werden müssen (z. b. eine Weltmatrix), werden in einen konstanten Puffer gruppiert, der für jedes Objekt aktualisiert werden kann. Dies ist von Daten getrennt, die eine Szene charakterisieren und daher wahrscheinlich viel seltener aktualisiert werden (wenn sich die Szene ändert).


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



### <a name="default-constant-buffers"></a>Standardmäßige Konstante Puffer

Es sind zwei standardmäßige Konstante Puffer verfügbar, $Global und $param. Variablen, die im globalen Gültigkeitsbereich abgelegt werden, werden dem $Global cBuffer implizit hinzugefügt. dabei wird dieselbe Verpackungsmethode verwendet, die für cbuffers verwendet wird. Einheitliche Parameter in der Parameterliste einer Funktion werden im $param Konstanten Puffer angezeigt, wenn ein Shader außerhalb des Effects-Frameworks kompiliert wird. Bei der Kompilierung innerhalb des Effects-Frameworks müssen alle Uniformen in Variablen aufgelöst werden, die im globalen Gültigkeitsbereich definiert sind.

## <a name="examples"></a>Beispiele

Im folgenden finden Sie ein Beispiel aus [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) , bei dem es sich um einen Textur Puffer handelt, der aus einem Array von Matrizen besteht.


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



Diese Beispiel Deklaration weist manuell einen konstanten Puffer zu, um bei einem bestimmten Register zu beginnen, und packt auch bestimmte Elemente nach unter Komponenten.


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

 

