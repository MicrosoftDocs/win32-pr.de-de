---
title: Klonen eines Effekts
description: Beim Klonen eines Effekts wird eine zweite, fast identische Kopie des Effekts erstellt.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195b4e9a42e595558acc4c512f8662c11b2acde7873e123b242ee272eeea7e8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538004"
---
# <a name="cloning-an-effect"></a>Klonen eines Effekts

Beim Klonen eines Effekts wird eine zweite, fast identische Kopie des Effekts erstellt. Im folgenden einzelnen Qualifizierer finden Sie eine Erklärung, warum er nicht genau ist. Eine zweite Kopie eines Effekts ist nützlich, wenn das Effektframework auf mehreren Threads verwendet werden soll, da die Effektlaufzeit nicht threadsicher ist, um eine hohe Leistung zu gewährleisten.

Da Gerätekontexte auch nicht threadsicher sind, sollten verschiedene Threads unterschiedliche Gerätekontexte an die ID3DX11EffectPass::Apply-Methode übergeben.

Ein Effekt kann mit der folgenden Syntax geklont werden:


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



Im obigen Beispiel kapselt die geklonte Kopie denselben Zustand wie der ursprüngliche Effekt, unabhängig davon, in welchem Zustand sich der ursprüngliche Effekt befindet. Dies gilt insbesondere für:

1.  Wenn pEffect optimiert ist, wird pCloned Effect optimiert.
2.  Wenn pEffect über einige vom Benutzer verwaltete Variablen verfügt, verfügt pCloned Effect über die gleichen vom Benutzer verwalteten Variablen (siehe einzelne Beschreibung unten).
3.  Alle ausstehenden Variablenupdates (bis ein Apply-Aufruf den Gerätestatus aktualisiert) in pEffect stehen in pClonedEffect aus.

Die folgenden Direct3D 11-Geräteobjekte sind unveränderlich oder werden vom Effektframework nie aktualisiert, sodass der geklonte Effekt auf dieselben Objekte wie der ursprüngliche Effekt verweisen wird:

1.  Zustandsblockobjekte (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)
2.  Shader
3.  Klasseninstanzen
4.  Texturen (ohne Texturpuffer)
5.  Ungeordnete Zugriffsansichten

Die folgenden Direct3D 11-Geräteobjekte sind sowohl unveränderlich als auch von der Effect Runtime geändert (es sei denn, der Benutzer verwaltet oder ist in einem geklonten Effekt einzeln); Neue Kopien dieser Objekte werden erstellt, wenn sie nicht einzeln sind:

1.  Konstante Puffer
2.  Texturpuffer

## <a name="single-constant-buffers-and-texture-buffers"></a>Einzelne Konstantenpuffer und Texturpuffer

Beachten Sie, dass diese Diskussion sowohl für konstante Puffer als auch für Texturen gilt, aber es wird davon ausgegangen, dass konstanten Puffern das Lesen erleichtert.

Es kann Fälle geben, in denen ein konstanter Puffer nur von einem Thread aktualisiert wird, aber der durch geklonte Effekte festgelegte Gerätezustand diese Daten verwendet. Der Haupteffekt kann z. B. die Welt- und Ansichtsmatrizen aktualisieren, auf die von Shadern in geklonten Effekten verwiesen wird, die die Welt- und Ansichtsmatrizen nicht ändern. In diesen Fällen müssen die geklonten Effekte auf den aktuellen konstanten Puffer verweisen, anstatt einen neu zu erstellen.

Es gibt zwei Möglichkeiten, dieses gewünschte Ergebnis zu erzielen:

1.  Verwenden Sie ID3DX11EffectConstantBuffer::SetConstantBuffer für den geklonten Effekt, damit er vom Benutzer verwaltet wird.
2.  Markieren Sie den konstanten Puffer im HLSL-Code als "single", und erzwingen Sie, dass die Effect Runtime nach dem Klonen als vom Benutzer verwaltet behandelt wird.

Es gibt zwei Unterschiede zwischen den beiden oben genannten Methoden. Zunächst wird in Methode 1 ein neuer ID3D11Buffer erstellt und ein Benutzer erstellt, bevor SetConstantBuffer aufgerufen wird. Nach dem Aufruf von UndoSetConstantBuffer im geklonten Effekt zeigt die Variable in Methode 1 außerdem auf den neu erstellten Puffer (der sich auf Apply aktualisiert), während die Variable in Methode 2 weiterhin auf den ursprünglichen Puffer zeigt (ohne ihn bei Anwenden zu aktualisieren).

Sehen Sie sich das folgende Beispiel in HLSL an:


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



Beim Klonen erstellt der geklonte Effekt einen neuen ID3D11Buffer für ObjectData und füllt seinen Inhalt auf Anwenden aus, verweist aber auf den ursprünglichen ID3D11Buffer für ViewData. Der einzelne Qualifizierer kann beim Klonen ignoriert werden, indem das Flag D3DX11 EFFECT CLONE FORCE NONSINGLE (D3DX11 \_ EFFECT CLONE FORCE \_ \_ \_ NONSINGLE) festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




