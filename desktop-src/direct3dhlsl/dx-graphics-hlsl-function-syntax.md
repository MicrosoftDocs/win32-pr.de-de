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
ms.openlocfilehash: 7358a59dba0096f5c8ffe58072a974ebff9a1050
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390862"
---
# <a name="function-declaration-syntax"></a>Syntax der Funktionsdeklaration

HLSL-Funktionen werden mit der folgenden Syntax deklariert.



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| \[*Storageclass* \] \[clipplane () \] \[ präziser \] Rückgabe \_ Wert *Name* (Argument \[ *List* \] ) \[ : *Semantik* \] { \[ *Status Block* \] }; |



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*Storageclass*
</dt> <dd>

Ein Modifizierer, der eine Funktionsdeklaration neu definiert. **Inline** ist zurzeit der einzige Modifiziererwert. Der Modifiziererwert muss **Inline** sein, da er auch der Standardwert ist. Daher ist eine Funktion Inline, unabhängig davon, ob Sie **Inline** angeben und alle Funktionen in HLSL Inline sind. Eine Inline Funktion generiert eine Kopie des Funktions Texts (beim Kompilieren) für jeden Funktions Aufruf. Dies geschieht, um den mehr Aufwand für das Aufrufen der-Funktion zu verringern.

</dd> <dt>

<span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplane*
</dt> <dd>

Optionale Liste von Clip-Ebenen, die bis zu 6 vom Benutzer angegebene Clip Flächen sind. Dies ist ein alternativer Mechanismus für [SV \_ clipdistance](dx-graphics-hlsl-semantics.md) , der auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher funktioniert.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*
</dt> <dd>

Eine ASCII-Zeichenfolge, die den Namen der Shader-Funktion eindeutig identifiziert.

</dd> <dt>

<span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*Argument List*
</dt> <dd>

Optionale Argumentliste, eine durch Trennzeichen getrennte Liste von [Argumenten](dx-graphics-hlsl-function-parameters.md) , die an eine Funktion übermittelt werden.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Tischer*
</dt> <dd>

Optionale Zeichenfolge, die die beabsichtigte Verwendung der Rückgabe Daten identifiziert (siehe [Semantik (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*Status Block*
</dt> <dd>

Optionale [Anweisungen](dx-graphics-hlsl-statement-blocks.md) , die den Hauptteil der Funktion bilden. Eine Funktion, die ohne Text definiert ist, wird als Funktionsprototyp bezeichnet. der Text einer prototypfunktion muss an anderer Stelle definiert werden, bevor die Funktion aufgerufen werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabetyp kann einer dieser [HLSL-Typen](dx-graphics-hlsl-data-types.md)sein.

## <a name="remarks"></a>Bemerkungen

Die Syntax auf dieser Seite beschreibt fast alle Arten von HLSL-Funktionen, darunter Vertex-Shader, Pixel-Shader und Hilfsfunktionen. Obwohl ein Geometry-Shader auch mit einer Funktion implementiert wird, ist die Syntax etwas komplizierter, sodass eine separate Seite vorhanden ist, die eine Geometry-shaderfunktionsdeklaration definiert (siehe [Geometry-Shader-Objekt (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).

Eine Funktion kann überladen werden, solange Sie eine eindeutige Kombination aus Parametertypen und/oder Parameterreihenfolge erhält. HLSL implementiert auch eine Reihe integrierter oder [**intrinsischer Funktionen**](dx-graphics-hlsl-intrinsic-functions.md).

Sie können benutzerspezifische Clip-Ebenen mit dem **clipplane** -Attribut angeben. Diese Clip Flächen werden von Windows auf alle gezeichneten primitiven angewendet. Das **clipplane** -Attribut funktioniert wie [SV \_ clipdistance](dx-graphics-hlsl-semantics.md) , funktioniert jedoch auf allen Hardware [Funktionsebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher. Weitere Informationen finden Sie unter [User Clip Plane on Feature Level 9 Hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).

## <a name="examples"></a>Beispiele

Dieses Beispiel ist aus BasicHLSL10. FX aus dem [BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)-Beispiel.


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



Dieses Beispiel aus advancedpartikel. FX aus dem [advancedpartikel](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)-Beispiel veranschaulicht die Verwendung einer Semantik für den Rückgabetyp.


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

 

 