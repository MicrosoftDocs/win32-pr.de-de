---
title: Syntax der Funktionsdeklaration
description: HLSL-Funktionen werden mit der folgenden Syntax deklariert.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2781d173eb4a1c18a661495d9fb55a0cced81921
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998327"
---
# <a name="function-declaration-syntax"></a>Syntax der Funktionsdeklaration

HLSL-Funktionen werden mit der folgenden Syntax deklariert.



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| \[*StorageClass* \] \[clipplanes() \] \[ precise \] Return Value \_ *Name* ( \[ *ArgumentList* \] ) : \[ *Semantic* \] { \[ *StatementBlock* \] }; |



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*
</dt> <dd>

Modifizierer, der eine Funktionsdeklaration neu definiert. **Inline** ist derzeit der einzige Modifiziererwert. Der Modifiziererwert muss **inline** sein, da er auch der Standardwert ist. Daher ist eine Funktion inline, unabhängig davon, ob Sie **inline** angeben, und alle Funktionen in HLSL sind inline. Eine Inlinefunktion generiert eine Kopie des Funktionstexts (beim Kompilieren) für jeden Funktionsaufruf. Dies wird durchgeführt, um den Mehraufwand für den Aufruf der Funktion zu verringern.

</dd> <dt>

<span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*
</dt> <dd>

Optionale Liste der Clipebenen, d. h. bis zu sechs benutzerdefinierte Clipebenen. Dies ist ein alternativer Mechanismus für [SV \_ ClipDistance,](dx-graphics-hlsl-semantics.md) der auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher funktioniert.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Namen*
</dt> <dd>

Eine ASCII-Zeichenfolge, die den Namen der Shaderfunktion eindeutig identifiziert.

</dd> <dt>

<span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*Argumentlist*
</dt> <dd>

Optionale Argumentliste, bei der es sich um eine durch Kommas getrennte Liste von [Argumenten](dx-graphics-hlsl-function-parameters.md) handelt, die an eine Funktion übergeben werden.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantische*
</dt> <dd>

Optionale Zeichenfolge, die die beabsichtigte Verwendung der Rückgabedaten angibt (siehe [Semantik (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

Optionale [Anweisungen,](dx-graphics-hlsl-statement-blocks.md) die den Text der Funktion enthalten. Eine Funktion, die ohne Text definiert ist, wird als Funktionsprototyp bezeichnet. Der Text einer Prototypfunktion muss an anderer Stelle definiert werden, bevor die Funktion aufgerufen werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabetyp kann einer dieser [HLSL-Typen sein.](dx-graphics-hlsl-data-types.md)

## <a name="remarks"></a>Hinweise

Die Syntax auf dieser Seite beschreibt fast jeden Typ von HLSL-Funktion, einschließlich Vertex-Shadern, Pixel-Shadern und Hilfsfunktionen. Während ein Geometrie-Shader auch mit einer Funktion implementiert wird, ist seine Syntax etwas komplizierter, sodass es eine separate Seite gibt, die eine Deklaration einer Geometrie-Shaderfunktion definiert (siehe [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).

Eine Funktion kann überladen werden, solange sie eine eindeutige Kombination aus Parametertypen und/oder Parameter reihenfolge erhält. HLSL implementiert auch eine Reihe von integrierten oder [**systeminternen Funktionen.**](dx-graphics-hlsl-intrinsic-functions.md)

Sie können benutzerspezifische Clipebenen mit dem **Clipplanes-Attribut** angeben. Windows wendet diese Clipebenen auf alle gezeichneten Primitive an. Das **Clipplanes-Attribut** funktioniert wie [SV \_ ClipDistance,](dx-graphics-hlsl-semantics.md) funktioniert jedoch auf allen Hardwarefeatures [der](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Ebene 9 x \_ und höher. Weitere Informationen finden Sie unter User clip planes on feature level 9 hardware (Benutzeroberflächenebenen auf Hardware [auf Featureebene 9).](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)

## <a name="examples"></a>Beispiele

Dieses Beispiel ist von BasicHLSL10.fx aus dem [BasicHLSL10-Beispiel .](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



Dieses Beispiel aus AdvancedParticles.fx aus [dem AdvancedParticles-Beispiel](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)veranschaulicht die Verwendung einer Semantik für den Rückgabetyp.


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Funktionen (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 
