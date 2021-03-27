---
title: Klonen eines Effekts
description: Das Klonen eines Effekts erzeugt eine zweite, fast identische Kopie des Effekts.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68607d3cc9f00a346fcfa65c255f3caa51dea384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711705"
---
# <a name="cloning-an-effect"></a>Klonen eines Effekts

Das Klonen eines Effekts erzeugt eine zweite, fast identische Kopie des Effekts. Im folgenden einzelnen Qualifizierer finden Sie eine Erläuterung, warum dies nicht exakt ist. Eine zweite Kopie eines Effekts ist nützlich, wenn Sie das Effekten-Framework für mehrere Threads verwenden möchten, da die Effekt Laufzeit nicht Thread sicher ist, um eine hohe Leistung aufrechtzuerhalten.

Da Geräte Kontexte auch nicht Thread sicher sind, sollten verschiedene Threads verschiedene Geräte Kontexte an die ID3DX11EffectPass:: Apply-Methode übergeben.

Ein Effekt kann mit der folgenden Syntax geklont werden:


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



Im obigen Beispiel wird die geklonte Kopie denselben Zustand wie der ursprüngliche Effekt Kapseln, unabhängig davon, in welchem Zustand sich der ursprüngliche Effekt befindet. Dies gilt insbesondere für:

1.  Wenn "Peer-ffect" optimiert ist, wird der pgeklonte Effekt optimiert.
2.  Wenn für "Peer-ffect" einige vom Benutzer verwaltete Variablen vorhanden sind, haben die pgeklonten Effekte dieselben Benutzer verwalteten Variablen (siehe die Beschreibung unten).
3.  Alle ausstehenden Variablen Aktualisierungen (bis zum Update des Gerätestatus "Apply") in "pclonede ffect" stehen aus.

Die folgenden Direct3D 11-Geräte Objekte sind unveränderlich oder werden nie durch das Effects-Framework aktualisiert, sodass der geklonte Effekt auf die gleichen Objekte wie der ursprüngliche Effekt zeigt:

1.  State Block-Objekte (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)
2.  Shader
3.  Klassen Instanzen
4.  Texturen (ohne Textur Puffer)
5.  Ungeordnete Zugriffs Sichten

Die folgenden Direct3D 11-Geräte Objekte sind unveränderlich und werden von der Effekt Laufzeit geändert (es sei denn, vom Benutzer verwaltet oder Single in einem geklonten Effekt). neue Kopien dieser Objekte werden erstellt, wenn Sie nicht einzeln sind:

1.  Konstantenpuffer
2.  Textur Puffer

## <a name="single-constant-buffers-and-texture-buffers"></a>Einzelne Konstante Puffer und Textur Puffer

Beachten Sie, dass sich diese Erörterung auf Konstante Puffer und Texturen bezieht

In Fällen, in denen ein konstanter Puffer nur von einem Thread aktualisiert wird, werden diese Daten von einem Gerätezustand, der durch geklonte Effekte festgelegt wurde, verwendet. Der Haupteffekt kann z. b. die Welt aktualisieren und Matrizen anzeigen, auf die von Shadern in geklonten Effekten verwiesen wird, die nicht die Welt-und Ansichts Matrizen ändern. In diesen Fällen müssen die geklonten Effekte auf den aktuellen Konstanten Puffer verweisen, anstatt einen neu zu erstellen.

Es gibt zwei Möglichkeiten, dieses gewünschte Ergebnis zu erzielen:

1.  Verwenden Sie ID3DX11EffectConstantBuffer:: setconstantbuffer für den geklonten Effekt, damit er vom Benutzer verwaltet wird.
2.  Markieren Sie den konstanten Puffer im HLSL-Code als "Single", und erzwingen Sie, dass die Auswirkung der Laufzeit nach dem Klonen vom Benutzer verwaltet wird.

Es gibt zwei Unterschiede zwischen den beiden oben genannten Methoden. Zuerst wird in Methode 1 ein neuer ID3D11Buffer erstellt, und der Benutzer wird vor dem Aufruf von setconstantbuffer aufgerufen. Nach dem Aufrufen von undosetconstantbuffer im geklonten Effekt verweist die Variable in der Methode 1Auf den neu erstellten Puffer (die Auswirkungen werden bei Apply aktualisiert), während die Variable in der Methode 2 weiterhin auf den ursprünglichen Puffer zeigt (nicht bei der Übersetzung aktualisiert).

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



Beim Klonen wird durch den geklonten Effekt ein neuer ID3D11Buffer für ObjectData erstellt, und der Inhalt wird bei Apply ausgefüllt, aber auf den ursprünglichen ID3D11Buffer für ViewData verwiesen. Der einzelne Qualifizierer kann beim Klon Vorgang ignoriert werden, indem das \_ Flag "Bibliothek d3dx11 Effect \_ Clone \_ Force \_ nonsingle" festgelegt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




