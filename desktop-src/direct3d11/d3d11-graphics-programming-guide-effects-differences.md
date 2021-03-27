---
title: Unterschiede zwischen den Effekten 10 und Effekte 11
description: In diesem Thema werden die Unterschiede zwischen den Effekten 10 und den Effekten 11 veranschaulicht.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728232"
---
# <a name="differences-between-effects-10-and-effects-11"></a>Unterschiede zwischen den Effekten 10 und Effekte 11

In diesem Thema werden die Unterschiede zwischen den Effekten 10 und den Effekten 11 veranschaulicht.

## <a name="device-contexts-threading-and-cloning"></a>Geräte Kontexte, Threading und Klonen

Die ID3D10Device-Schnittstelle wurde in Direct3D 11 in zwei Schnittstellen aufgeteilt: ID3D11Device und Verknüpfung id3d11devicecontext aus. Sie können mehrere ID3D11DeviceContexts erstellen, um die gleichzeitige Ausführung für mehrere Threads zu vereinfachen. Effekte 11 erweitert dieses Konzept auf das Effects-Framework.

Die Auswirkung 11-Laufzeit ist ein Single Thread. Aus diesem Grund sollten Sie keine einzelne ID3DX11Effect-Instanz mit mehreren Threads gleichzeitig verwenden.

Wenn Sie die Effekte 11-Laufzeit für mehrere Instanzen verwenden möchten, müssen Sie separate ID3DX11Effect-Instanzen erstellen. Da Verknüpfung id3d11devicecontext aus auch Single Thread ist, sollten Sie bei Apply verschiedene Verknüpfung id3d11devicecontext aus-Instanzen an jede Effekt Instanz übergeben. Sie können diese separaten Geräte Kontexte verwenden, um Befehlslisten zu erstellen, damit der Renderingthread diese auf den unmittelbaren Gerätekontext anwenden kann.

Die einfachste Möglichkeit, mehrere Effekte zu erstellen, die dieselbe Funktionalität Kapseln, um Sie für mehrere Threads zu verwenden, besteht darin, einen Effekt zu erstellen und dann geklonte Kopien zu erstellen. Das Klonen bietet die folgenden Vorteile gegenüber der Erstellung mehrerer Kopien von Grund auf:

1.  Die Klon Routine ist schneller als die Erstellungs Routine.
2.  Die geklonten Effekte teilen sich die erstellten Shader, Zustands Blöcke und Klassen Instanzen (sodass Sie nicht neu erstellt werden müssen).
3.  Geklonte Effekte können Konstante Puffer gemeinsam verwenden.
4.  Geklonte Effekte beginnen mit dem Zustand, der mit dem aktuellen Effekt übereinstimmt (Variablen Werte, unabhängig davon, ob Sie optimiert wurden).

Weitere Informationen finden Sie unter [Klonen eines Effekts](d3d11-graphics-programming-guide-effects-cloning.md) .

## <a name="effect-pools-and-groups"></a>Effekt Pools und-Gruppen

Der weit verbreitete Gebrauch von Effekt Pools in Direct3D 10 war das Gruppieren von Material. Die Effekt Pools wurden aus den Effekten 11 entfernt, und Gruppen wurden hinzugefügt. Dies ist eine effizientere Methode zum Gruppieren von Material.

Eine Effekt Gruppe ist einfach eine Reihe von Techniken. Weitere Informationen finden Sie unter [Wirkungs Gruppen Syntax (Direct3D 11)](d3d11-effect-group-syntax.md) .

Sehen Sie sich die folgende Effekt Hierarchie mit vier untergeordneten Effekten und einem Effekt Pool an:


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



Sie können die gleichen Funktionen in den Effekten 11 durch die Verwendung von Gruppen erreichen:


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



## <a name="new-shader-stages"></a>Neue Shader-Stufen

Es gibt drei neue Shader-Stufen in Direct3D 11: den Hull-Shader, den Domänen-Shader und den Compute-Shader. Effekte 11 behandelt diese auf ähnliche Weise wie Vertex-Shader, Geometry-Shader und Pixel-Shader.

Der Auswirkung 11 wurden drei neue Variablen Typen hinzugefügt:

-   Hullshader
-   Domainshader
-   Computeshader

Wenn Sie diese Shader in einem Verfahren verwenden, müssen Sie die Technik "technique11" und nicht "technique10" bezeichnen. Der COMPUTE-Shader kann nicht im gleichen Durchlauf wie jeder andere Grafik Zustand (andere Shader, Zustands Blöcke oder Renderziele) festgelegt werden.

## <a name="new-texture-types"></a>Neue Textur Typen

Direct3D 11 unterstützt die folgenden Textur Typen:

-   [Appendstructuredbuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [Byteaddressbuffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [Consumestructuredbuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [Structuredbuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a>Ungeordnete Zugriffs Sichten

Effekte 11 unterstützt das Abrufen und Festlegen der neuen ungeordneten Zugriffs Ansichts Typen. Dies funktioniert auf ähnliche Weise wie Texturen.

Sehen Sie sich das HLSL-Beispiel an:


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



Direct3D 11 unterstützt die folgenden ungeordneten Zugriffs Ansichts Typen:

-   Rwbuffer
-   Rwbyteaddressbuffer
-   Rwstructuredbuffer
-   RWTexture1D
-   RWTexture1DArray
-   RWTexture2D
-   RWTexture2DArray
-   RWTexture3D

## <a name="interfaces-and-class-instances"></a>Schnittstellen und Klassen Instanzen

Informationen zur Schnittstelle und Klassen Syntax finden Sie unter [Schnittstellen und Klassen](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

Informationen zum Verwenden von Schnittstellen und Klassen in Effekten finden Sie unter [Schnittstellen und Klassen in Effekten](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).

## <a name="addressable-stream-out"></a>Adressier barer Datenstrom ausgehend

In Direct3D 10 konnten Geometry-Shader einen Datenstrom an die Stream-Ausgabe Einheit und die Raster-Einheit ausgeben. In Direct3D11 können Geometry-Shader bis zu vier Datenströme in die Datenstrom Ausgabe Einheit ausgeben, und höchstens einer dieser Datenströme an die Raster-Einheit. Die systeminterne **konstruktgswithso** -Funktion wurde aktualisiert, um diese neue Funktion widerzuspiegeln.

Weitere Informationen finden [Sie unter Stream out-Syntax](d3d11-graphics-reference-effect-streamout.md) .

## <a name="setting-and-unsetting-device-state"></a>Festlegen und Zurücksetzen des Gerätestatus

In den Effekten 10 könnten Sie Konstante Puffer und Textur Puffer mithilfe der [**ID3D10EffectConstantBuffer:: setconstantbuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) -und [**settexturebuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) -Funktionen vom Benutzer verwaltet werden. Nachdem Sie diese Funktionen aufgerufen haben, verwaltet die Runtime 10 Runtime nicht mehr den konstanten Puffer oder Textur Puffer, und der Benutzer muss die Daten mithilfe der ID3D10Device-Schnittstelle ausfüllen.

In Auswirkung 11 können Sie auch die Zustands Blöcke (Blend-Status, Status des Rasterizers, tiefen Schablone und samplerstatus) mithilfe der folgenden Aufrufe erstellen:

-   [**ID3DX11EffectBlendVariable:: setblendstate**](id3dx11effectblendvariable-setblendstate.md)
-   [**ID3DX11EffectRasterizerVariable:: tartrasterizerstate**](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable:: setdepthstencilstate**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable:: setsampler**](id3dx11effectsamplervariable-setsampler.md)

Nachdem Sie diese Funktionen aufgerufen haben, werden die Block Variablen in der Auswirkung 11 nicht mehr verwaltet, und die Werte bleiben unverändert. Beachten Sie, dass der Benutzer einen neuen Zustands Block festlegen muss, um die Werte zu ändern, da Zustands Blöcke unveränderlich sind.

Sie können auch Konstante Puffer, Textur Puffer und Zustands Blöcke auf den Nichtbenutzer verwalteten Zustand zurücksetzen. Wenn Sie diese Variablen nicht mehr festlegen, werden Sie von der Common Language Runtime bei Bedarf weiterhin aktualisiert. Mit den folgenden aufrufen können Sie vom Benutzer verwaltete Variablen nicht festlegen:

-   [**ID3DX11EffectConstantBuffer:: undosetconstantbuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [**ID3DX11EffectConstantBuffer:: undosettexturebuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [**ID3DX11EffectBlendVariable:: undosetblendstate**](id3dx11effectblendvariable-undosetblendstate.md)
-   [**ID3DX11EffectRasterizerVariable:: undotartrasterizerstate**](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable:: undosetdepthstencilstate**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable:: undosetsampler**](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a>Auswirkungen virtueller Computer

Die Auswirkungen der virtuellen Maschine, die komplexe Ausdrücke außerhalb der Funktionen ausgewertet hat, wurden entfernt.

Die folgenden Beispiele für komplexe Ausdrücke werden nicht unterstützt:

1.  Setpixelshader (mypsarray (i \* 3 + j));
2.  Setpixelshader (mypsarray ((float) i);
3.  Filter = i + 2;

Die folgenden Beispiele für nicht komplexe Ausdrücke werden unterstützt:

1.  Setpixelshader (myps);
2.  Setpixelshader (myps \[ i \] );
3.  Setpixelshader (myps \[ uindex \] );//uindex ist eine uint-Variable.
4.  Filter = i;
5.  Filter = anisotrope;

Diese Ausdrücke können in Zustands Block Ausdrücken (z. b. Filter) und Pass Ausdrücken (z. b. setpixelshader) vorkommen.

## <a name="source-availability-and-location"></a>Quell Verfügbarkeit und-Speicherort

Die Auswirkungen 10 wurden in D3D10.dll verteilt. Die Effekte 11 werden als Quelle und mit entsprechenden Visual Studio-Projektmappen verteilt, um Sie zu kompilieren. Wenn Sie Effekte vom Typ Anwendungen erstellen, empfiehlt es sich, die Effekte 11-Quelle direkt in diese Anwendungen einzubeziehen.

Sie können die Effekte 11 von den [Effekten für das Update von Direct3D 11](https://github.com/Microsoft/FX11)erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 