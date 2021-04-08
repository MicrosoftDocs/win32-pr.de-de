---
description: Das Vertex Shader 3,0-Modell unterstützt die Textur Suche im Vertex-Shader mithilfe der texldl-vs-Textur Lade Anweisung.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Scheitelpunkt Texturen in vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e8e7bbf7e1ae9764fe5b30647f318dfaeb3ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747160"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a>Scheitelpunkt Texturen in vs \_ 3 \_ 0 (DirectX HLSL)

Das Vertex Shader 3,0-Modell unterstützt die Textur Suche im Vertex-Shader mithilfe der [texldl-vs-](../direct3dhlsl/texldl---vs.md) Textur Lade Anweisung. Die Vertex-Engine enthält vier textursampler-Phasen mit den Namen [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 und D3DVERTEXTEXTURESAMPLER3. Diese unterscheiden sich von der Verschiebung des Verschiebungs Karten Samplern und der Textur Samplern in der Pixel-Engine.

Zum Beispiel für Texturen, die in diesen vier Phasen festgelegt werden, können Sie die Vertex-Engine verwenden und die Phasen mit der [**CheckDeviceFormat**](/windows/desktop/api) -Methode programmieren. Legen Sie mithilfe von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)Texturen in diesen Phasen fest, wobei Sie den Phasen Index [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) bis D3DVERTEXTEXTURESAMPLER3 verwenden. Ein neues Register wurde im Vertex-Shader eingeführt, das Samplerregister (wie in PS \_ 2 \_ 0), das den Scheitelpunkt Textur Sampler darstellt. Dieses Register muss im Shader definiert werden, bevor es verwendet werden kann.

Eine Anwendung kann Abfragen, wenn ein Format als vertextextur unterstützt wird, indem [**CheckDeviceFormat**](/windows/desktop/api) mit [D3DUSAGE \_ Query \_ vertextexture](d3dusage-query.md)aufgerufen wird.

> [!Note]  
> Dabei handelt es sich um ein abfrageflag, sodass es in keiner der Funktionen von "-Funktion" akzeptiert wird. Eine im Standard Pool erstellte Scheitelpunkt Textur kann als Pixel Textur festgelegt werden und umgekehrt. Um jedoch die Verarbeitung der Software Scheitel Punkte zu verwenden, muss die Vertex-Textur im Scratch-Pool erstellt werden (unabhängig davon, ob es sich um ein Gerät mit gemischtem Modus oder ein Software-Vertex-Verarbeitungs Gerät handelt).

 

Die Funktionalität ist mit den Pixel Texturen identisch, mit Ausnahme der folgenden:

-   Die anisotrope Textur Filterung wird nicht unterstützt. daher \_ wird D3DSAMP MaxAnisotropy ignoriert, und D3DTEXF \_ anisotrope kann nicht für die Vergrößerung festgelegt werden, oder es kann für diese Phasen nicht minimal festgelegt werden.
-   Die Rate der Änderungs Informationen ist nicht verfügbar. Daher muss die Anwendung die Detailebene berechnen und diese Informationen als Parameter für [texldl-vs](../direct3dhlsl/texldl---vs.md)bereitstellen.

Es gelten folgende Beschränkungen:

-   Wie bei Pixel-Shadern \_ wird D3DSAMP Elementindex verwendet, um herauszufinden, aus welchem Element ein Beispiel entnommen werden soll, wenn multielementtexturen unterstützt werden.
-   Der Status "D3DSAMP \_ dmapoffset" wird für diese Phasen ignoriert.
-   Verwenden Sie [**CheckDeviceFormat**](/windows/desktop/api) mit [D3DUSAGE \_ Query \_ vertextexture "](d3dusage-query.md) , um eine Textur abzufragen, um festzustellen, ob Sie als vertextextur verwendet werden kann.
-   Vertextexturefiltercaps gibt an, welche Art von Filtern bei den Scheitelpunkt Textur-Samplern zulässig sind. [D3DPTFILTERCAPS \_ Minsanisotropic](d3dptfiltercaps.md) und D3DPTFILTERCAPS \_ magsanisotrope sind nicht zulässig.

## <a name="sampling-stage-registers"></a>Abtast Phasen Register

Ein Sampling-Phasen Register identifiziert eine samplingeinheit, die in Textur Ladeanweisungen verwendet werden kann. Eine samplingeinheit entspricht der Phase Textur Sampling und kapselt den in [**setsamplerstate angegebenen samplingspezifischen**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)Zustand.

Jeder Sampler identifiziert eindeutig eine einzelne Textur Oberfläche, die auf den entsprechenden Sampler mithilfe von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)festgelegt wird. Allerdings kann die gleiche Textur Oberfläche bei mehreren Samplers festgelegt werden.

Bei der zeichnungszeit kann eine Textur nicht gleichzeitig als Renderziel und Textur in einer Phase festgelegt werden.

Da vs \_ 3 \_ 0 vier Samplers unterstützt, können bis zu vier Textur Oberflächen in einem einzelnen shaderdurchlauf aus gelesen werden. Ein Samplerregister kann nur als Argument in der Textur Lade Anweisung angezeigt werden: [texldl-vs](../direct3dhlsl/texldl---vs.md).

\_Wenn Sie in vs 3 \_ 0 einen Sampler verwenden, muss er am Anfang des Shader-Programms mit dem [DCL- \_ samplertype (SM3-vs ASM)](../direct3dhlsl/dcl-samplertype---vs.md) deklariert werden (wie in PS \_ 2 \_ 0).

## <a name="software-processing"></a>Software Verarbeitung

Diese Funktion wird bei der Verarbeitung von Software Scheitel Punkten unterstützt. Die unterstützten Filtertypen können überprüft werden, indem [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) aufgerufen und vertextexturefiltercaps überprüft wird. Alle veröffentlichten Textur Formate werden als Scheitelpunkt Texturen bei der Verarbeitung von Software Scheitel Punkten unterstützt.

Mithilfe von [**CheckDeviceFormat**](/windows/desktop/api) und Bereitstellen von (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ softwareprocessing**](d3dusage.md)) als Verwendung können Anwendungen überprüfen, ob ein bestimmtes Textur Format im Software Scheitelpunkt Verarbeitungsmodus unterstützt wird. Alle Formate werden für die Verarbeitung von Software Scheitel Punkten unterstützt. Der Scratch-Pool ist für die Verarbeitung von Software Scheitel Punkten erforderlich.

## <a name="api-changes"></a>API-Änderungen


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunkt Pipeline](vertex-pipeline.md)
</dt> </dl>

 

 
