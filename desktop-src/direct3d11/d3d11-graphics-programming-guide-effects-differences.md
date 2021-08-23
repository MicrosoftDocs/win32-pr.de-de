---
title: Unterschiede zwischen Effekten 10 und Effekten 11
description: In diesem Thema werden die Unterschiede zwischen Effekten 10 und Effects 11 erläutert.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b488015deae8cc93b9bc692c49d66ff1510bcc5639047fe253265be5b382a85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990120"
---
# <a name="differences-between-effects-10-and-effects-11"></a>Unterschiede zwischen Effekten 10 und Effekten 11

In diesem Thema werden die Unterschiede zwischen Effekten 10 und Effects 11 erläutert.

## <a name="device-contexts-threading-and-cloning"></a>Gerätekontexte, Threading und Klonen

Die ID3D10Device-Schnittstelle wurde in Direct3D 11 in zwei Schnittstellen unterteilt: ID3D11Device und ID3D11DeviceContext. Sie können mehrere ID3D11DeviceContexts erstellen, um die gleichzeitige Ausführung in mehreren Threads zu ermöglichen. Effekte 11 erweitert dieses Konzept auf das Effects-Framework.

Die Effects 11-Runtime ist singlethreaded. Aus diesem Grund sollten Sie keine einzelne ID3DX11Effect-Instanz mit mehreren Threads gleichzeitig verwenden.

Um die Effects 11-Runtime auf mehreren Instanzen zu verwenden, müssen Sie separate ID3DX11Effect-Instanzen erstellen. Da id3D11DeviceContext ebenfalls singlethreaded ist, sollten Sie bei Anwenden verschiedene ID3D11DeviceContext-Instanzen an jede Effect-Instanz übergeben. Sie können diese separaten Gerätekontexte verwenden, um Befehlslisten zu erstellen, sodass der Renderingthread sie auf den unmittelbaren Gerätekontext anwenden kann.

Die einfachste Möglichkeit, mehrere Effekte zu erstellen, die dieselbe Funktionalität kapseln, für die Verwendung in mehreren Threads, besteht darin, einen Effekt zu erstellen und dann geklonte Kopien zu erstellen. Das Klonen hat gegenüber dem Erstellen mehrerer Kopien von Grund auf die folgenden Vorteile:

1.  Die Klonroutine ist schneller als die Erstellungsroutine.
2.  Geklonte Effekte nutzen erstellte Shader, Zustandsblöcke und Klasseninstanzen gemeinsam (sodass sie nicht neu erstellt werden müssen).
3.  Geklonte Effekte können konstante Puffer gemeinsam nutzen.
4.  Geklonte Effekte beginnen mit dem Zustand, der dem aktuellen Effekt entspricht (Variablenwerte, unabhängig davon, ob sie optimiert wurden oder nicht).

Weitere Informationen finden Sie unter [Klonen eines Effekts.](d3d11-graphics-programming-guide-effects-cloning.md)

## <a name="effect-pools-and-groups"></a>Auswirkungspools und -gruppen

Die mit Abstand häufigste Verwendung von Effektpools in Direct3D 10 war für die Gruppierung von Materialien. Effektpools wurden aus Effekt 11 entfernt, und Gruppen wurden hinzugefügt. Dies ist eine effizientere Methode zum Gruppieren von Materialien.

Eine Effektgruppe ist einfach eine Reihe von Techniken. Weitere Informationen finden Sie unter [Effect Group Syntax (Direct3D 11) (Effektgruppensyntax (Direct3D 11)).](d3d11-effect-group-syntax.md)

Betrachten Sie die folgende Effekthierarchie mit vier untergeordneten Effekten und einem Effektpool:


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



Sie können die gleiche Funktionalität in Effects 11 mithilfe von Gruppen erreichen:


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a>Neue Shaderstufen

Es gibt drei neue Shaderstufen in Direct3D 11: den Hüllen-Shader, den Domänen-Shader und den Compute-Shader. Effekte 11 behandelt diese auf ähnliche Weise wie Vertex-Shader, Geometrie-Shader und Pixel-Shader.

Effects 11 wurden drei neue Variablentypen hinzugefügt:

-   HullShader
-   DomainShader
-   ComputeShader

Wenn Sie diese Shader in einer Technik verwenden, müssen Sie diese Technik "technique11" und nicht "technique10" bezeichnen. Der Compute-Shader kann nicht im selben Durchlauf wie jeder andere Grafikzustand (andere Shader, Zustandsblöcke oder Renderziele) festgelegt werden.

## <a name="new-texture-types"></a>Neue Texturtypen

Direct3D 11 unterstützt die folgenden Texturtypen:

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a>Ungeordnete Zugriffsansichten

Effekte 11 unterstützt das Abrufen und Festlegen der neuen ungeordneten Zugriffsansichtstypen. Dies funktioniert auf ähnliche Weise wie Texturen.

Betrachten Sie dieses HLSL-Beispiel für Effekte:


```
  
RWTexture1D<float> myUAV;
```



Sie können diese Variable in C++ wie folgt festlegen:


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



Direct3D 11 unterstützt die folgenden ungeordneten Zugriffsansichtstypen:

-   Rwbuffer
-   RWByteAddressBuffer
-   RWStructuredBuffer
-   RWTexture1D
-   RWTexture1DArray
-   RWTexture2D
-   RWTexture2DArray
-   RWTexture3D

## <a name="interfaces-and-class-instances"></a>Schnittstellen und Klasseninstanzen

Informationen zur Schnittstellen- und Klassensyntax finden Sie unter [Schnittstellen und Klassen.](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class)

Informationen zur Verwendung von Schnittstellen und Klassen in Effekten finden Sie unter [Schnittstellen und Klassen in Effekten.](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md)

## <a name="addressable-stream-out"></a>Adressierbarer Stream out

In Direct3D 10 konnten Geometrie-Shader einen Datenstrom an die Streamausgabeeinheit und die Rasterizereinheit ausgeben. In Direct3D11 können Geometrie-Shader bis zu vier Datenströme an die Streamausgabeeinheit und höchstens einen dieser Datenströme an die Rasterizereinheit ausgeben. Die systeminterne **ConstructGSWithSO-Funktion** wurde aktualisiert, um diese neue Funktionalität widerzuspiegeln.

Weitere Informationen finden Sie unter [Stream Out-Syntax.](d3d11-graphics-reference-effect-streamout.md)

## <a name="setting-and-unsetting-device-state"></a>Festlegen und Aufheben des Gerätestatus

In Effects 10 können Sie konstante Puffer und Texturpuffer benutzerverwaltet erstellen, indem Sie die Funktionen [**ID3D10EffectConstantBuffer::SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) und [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) verwenden. Nachdem Sie diese Funktionen aufgerufen haben, verwaltet die Effects 10-Runtime den Konstantenpuffer oder Texturpuffer nicht mehr, und der Benutzer muss die Daten mithilfe der ID3D10Device-Schnittstelle füllen.

In Effekten 11 können Sie die Zustandsblöcke (Blendzustand, Rasterizerzustand, Tiefenschablonenzustand und Samplerzustand) auch benutzerverwalten, indem Sie die folgenden Aufrufe verwenden:

-   [**ID3DX11EffectBlendVariable::SetBlendState**](id3dx11effectblendvariable-setblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::SetSampler**](id3dx11effectsamplervariable-setsampler.md)

Nachdem Sie diese Funktionen aufgerufen haben, verwaltet die Effects 11-Runtime die Zustandsblockvariablen nicht mehr, und die Werte bleiben unverändert. Da Zustandsblöcke unveränderlich sind, muss der Benutzer einen neuen Zustandsblock festlegen, um die Werte zu ändern.

Sie können auch konstante Puffer, Texturpuffer und Zustandsblöcke in den nicht vom Benutzer verwalteten Zustand zurücksetzen. Wenn Sie diese Variablen nicht festlegen, werden sie von der Effects 11-Runtime bei Bedarf weiterhin aktualisiert. Sie können die folgenden Aufrufe von nicht vom Benutzer verwalteten Variablen verwenden:

-   [**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [**ID3DX11EffectBlendVariable::UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a>Auswirkungen virtueller Computer

Die Auswirkungen des virtuellen Computers, der komplexe Ausdrücke außerhalb von Funktionen ausgewertet hat, wurden entfernt.

Die folgenden Beispiele für komplexe Ausdrücke werden nicht unterstützt:

1.  SetPixelShader( myPSArray( i \* 3 + j ) );
2.  SetPixelShader( myPSArray( (float)i );
3.  FILTER = i + 2;

Die folgenden Beispiele für nicht komplexe Ausdrücke werden unterstützt:

1.  SetPixelShader( myPS );
2.  SetPixelShader( myPS \[ i \] );
3.  SetPixelShader( myPS \[ uIndex \] ); :// uIndex ist eine uint-Variable
4.  FILTER = i;
5.  FILTER = ANISOTROP;

Diese Ausdrücke können in Zustandsblockausdrücken (z. B. FILTER) auftreten und Ausdrücke übergeben (z. B. SetPixelShader).

## <a name="source-availability-and-location"></a>Quellverfügbarkeit und Standort

Effekte 10 wurde in D3D10.dll verteilt. Effekte 11 wird als Quelle verteilt, mit entsprechenden Visual Studio Lösungen, um sie zu kompilieren. Wenn Sie Anwendungen vom Typ effects erstellen, empfiehlt es sich, die Effects 11-Quelle direkt in diese Anwendungen aufzunehmen.

Sie können Effekte 11 unter [Effekte für Direct3D 11 Update erhalten.](https://github.com/Microsoft/FX11)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 