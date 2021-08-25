---
description: Die folgenden Features wurden in Microsoft Direct3D 9 geändert. Wenn Sie diese Features verwenden, helfen Ihnen die unten aufgeführten Änderungen beim Portieren Ihrer Anwendung zu Direct3D 9 weiter.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Konvertieren in Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdf5ec812ede4e9d5d356d36b01bbcfcc7732fdb5946e2a13af90c9d9428fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850530"
---
# <a name="converting-to-direct3d-9"></a>Konvertieren in Direct3D 9

Die folgenden Features wurden in Microsoft Direct3D 9 geändert. Wenn Sie diese Features verwenden, helfen Ihnen die unten aufgeführten Änderungen beim Portieren Ihrer Anwendung zu Direct3D 9 weiter.

-   [BaseVertexIndex-Änderungen](#basevertexindex-changes)
-   [CreateImageSurface-Änderungen](#createimagesurface-changes)
-   [D3DENUM \_ NO \_ WHQL \_ LEVEL Changes](/windows)
-   [Erstellen von Ressourcenänderungen](#create-resource-changes)
-   [EnumAdapterModes-Änderungen](#enumadaptermodes-changes)
-   [Get/SetStreamSource-Änderungen \_](#getsetstreamsource-changes)
-   [Qualitätsänderungen für Multisampling](#multisampling-quality-changes)
-   [ResourceManagerDiscardBytes Changes](#resourcemanagerdiscardbytes-changes)
-   [SetSoftwareVertexProcessing Changes](#setsoftwarevertexprocessing-changes)
-   [Änderungen am Textur-Sampler](#texture-sampler-changes)
-   [Änderungen an der Vertexdeklaration](#vertex-declaration-changes)
-   [Intervalle \_ und \_ SwapEffects-Änderungen \_](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a>BaseVertexIndex-Änderungen

In DirectX 8.x erforderte IDirect3DDevice8::SetIndices einen Zeiger auf den Indexpuffer und einen BaseVertexIndex für die Anfangsposition im Scheitelpunktpuffer. Eine Anwendung, die verschiedene Objekte in den Scheitelpunktpuffer batchet, musste den Indexpuffer wechseln (oder IDirect3DDevice8::SetIndices aufrufen), bevor IDirect3DDevice8::D rawIndexedPrimitive aufgerufen wurde.

In Direct3D 9 wurde die Anfangsposition im Scheitelpunktpuffer *BaseVertexIndex* in IDirect3DDevice9::D rawIndexedPrimitive verschoben, und der Datentyp wurde von einem DWORD in einen INT geändert.


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a>CreateImageSurface-Änderungen

IDirect3DDevice8::CreateImageSurface wurde in [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)umbenannt. Ein zusätzlicher Parameter, der den D3DPOOL-Typ annimmt, wurde hinzugefügt. D3DPOOL \_ SCRATCH gibt eine Oberfläche zurück, die identische Eigenschaften wie eine von IDirect3DDevice8::CreateImageSurface erstellte Oberfläche aufweist. D3DPOOL \_ DEFAULT ist der geeignete Pool für die Verwendung mit [**StretchRect**](/windows/desktop/api) und [**ColorFill.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill)

## <a name="d3denum_no_whql_level-changes"></a>D3DENUM \_ NO \_ WHQL \_ LEVEL Changes

Anwendungen müssen jetzt explizit die Microsoft Windows Hardware Quality Labs (WHQL) anfordern, da die Antwort relativ lange dauert (einige Sekunden). D3DENUM \_ NO \_ WHQL \_ LEVEL wurde entfernt, und D3DENUM \_ WHQL \_ LEVEL wurde hinzugefügt.

## <a name="create-resource-changes"></a>Erstellen von Ressourcenänderungen

Ein Handle wurde mehreren Methoden hinzugefügt und sollte auf **NULL** festgelegt werden. Folgende Methoden sind betroffen:

-   [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [**CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a>EnumAdapterModes-Änderungen

[**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) nimmt jetzt ein D3DFORMAT an.


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



Das Format unterstützt einen erweiternden Satz von Anzeigemodi. Um Anwendungen vor dem Aufzählen von Formaten zu schützen, die bei der Auslieferung der Anwendung nicht zusammengestellt wurden, muss die Anwendung Direct3D das Format für die Anzeigemodi mitteilen, die aufzählt werden sollen. Das resultierende Array von Anzeigemodi unterscheidet sich nur durch Breite, Höhe und Aktualisierungsrate.

Die Anwendung gibt ein Pixelformat an, und die Enumeration ist auf die Anzeigemodi beschränkt, die genau dem Format entsprechen. Im Folgenden sind die zulässigen Formate aufgeführt:

-   D3DFMT \_ A1R5G5B5
-   D3DFMT \_ A2B10G10R10
-   D3DFMT \_ A8R8G8B8
-   D3DFMT \_ R5G6B5
-   D3DFMT \_ X1R5G5B5
-   D3DFMT \_ X8R8G8B8

Enumeration ist äquivalent für Alpha- und Nonalpha-Versionen des gleichen Formats. Das zurückgegebene Format wird immer mit dem gleichen Format gefüllt, das von der Anwendung bereitgestellt wird.

Diese Methode behandelt 565 und 555 als gleichwertig und gibt die richtige Version im Format zurück. Der Unterschied kommt nur ins Spiel, wenn die Anwendung den Hintergrundpuffer sperrt und ein explizites Flag vorhanden ist, das die Anwendung festlegen muss, um dies zu erreichen.

## <a name="getsetstreamsource-changes"></a>Get/SetStreamSource-Änderungen

Den [**Methoden GetStreamSource**](/windows/desktop/api) und [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) wurde ein Parameter hinzugefügt. Der Offset ist die Anzahl der Bytes zwischen dem Anfang des Streams und dem Anfang der Scheitelpunktdaten. Der entsprechende Wert wird in „Bytes“ angegeben. Dadurch kann die Pipeline Streamoffsets unterstützen. Informationen dazu, ob das Gerät Streamoffsets unterstützt, finden Sie unter D3DDEVCAPS2 \_ STREAMOFFSET.


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a>Qualitätsänderungen für Multisampling

Zuvor gab es nur die D3DMULTISAMPLE \_ TYPE-Enumeration. Direct3D 9 behält diese Enumeration bei und fügt die Idee einer Qualitätsstufe für jedes Element der Enumeration hinzu. Die Qualitätsstufe gibt einen Ausgleich zwischen visueller Qualität und Leistung an, indem die Anzahl der maskierbaren Stichproben (im Sinne von D3DRS \_ MULTISAMPLEMASK) angegeben wird.

Eine Anwendung sollte auswählen, wie viele maskierbare Stichproben sie benötigt, und dann pQualityLevels konsultieren. Wenn der Wert ungleich 0 (null) ist, gibt dieser Wert die Anzahl der Qualitätsstufen an, die die Anwendung über MultiSampleQuality an die verschiedenen Erstellungsfunktionen übergeben kann. Da Treiber alle multisample-Schemas als Qualitätsstufen bei D3DMULTISAMPLE \_ NONMASKABLE verfügbar machen, können Sie alle verfügbaren Multisamplingschemas durch diesen einen Typ aufzählen, wenn Ihre Anwendung keine Stichproben maskieren muss.

Das D3DPRASTERCAPS \_ STRETCHBLTMULTISAMPLE Caps-Bit wurde eingestellt. Dieses Bit bedeutet, dass die Multisamplingmethode keine Schreibmasken unterstützt und zwischen [**BeginScene**](/windows/desktop/api) und [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene)nicht ein- und ausgeschaltet werden konnte. Solche nichtmaskierbaren Methoden werden jetzt über D3DMULTISAMPLE \_ NONMASKABLE verfügbar gemacht.


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



Für jede Anzahl von maskierbaren Stichproben gibt es einen anderen Höchstwert. Beispiel: D3DMULTISAMPLE \_ 4 \_ SAMPLES kann drei Qualitätsstufen aufweisen, während D3DMULTISAMPLE \_ 2 SAMPLES nur \_ eins aufweisen kann. Es gibt höchstens acht Qualitätsstufen für jede Anzahl von maskierbaren Stichproben (der Treiber darf nicht mehr ausdrücken). Die Qualität reicht von 0 bis ( \* pQualityLevels – 1).

## <a name="resourcemanagerdiscardbytes-changes"></a>ResourceManagerDiscardBytes Changes

ResourceManagerDiscardBytes wurde durch IDirect3DDevice9::EvictManagedResources ersetzt. Es können alle Ressourcen entfernt werden, sowohl Direct3D- als auch Treiberressourcen.

Der Ressourcen-Manager wird nun abgefragt, wenn bei der Erstellung einer Ressource (verwaltet oder nicht verwaltet) ein Fehler auftritt, weil nicht genügend Videospeicher vorhanden ist. Der Manager wird automatisch aufgefordert, genügend Ressourcen frei zu geben, damit die Erstellung erfolgreich ist. In DirectX 8.0 war dies kein automatisierter Prozess.

## <a name="setsoftwarevertexprocessing-changes"></a>SetSoftwareVertexProcessing Changes

Eine Anwendung kann ein Gerät im gemischten Modus erstellen, um die Verarbeitung von Software- und Hardwarevertex zu verwenden.

Um zwischen den beiden Vertexverarbeitungsmodi in DirectX 8.x zu wechseln, rufen Sie IDirect3DDevice8::SetRenderState auf. Dies wurde durch [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) ersetzt, um Probleme zu beheben, die durch Zustandsblöcke verursacht werden. Diese neue Methode wird nicht von Zustandsblöcken aufgezeichnet.

## <a name="texture-sampler-changes"></a>Änderungen am Textur-Sampler

Direct3D 9 unterstützt bis zu 16 Texturoberflächen in einem Durchlauf mit dem Pixelshader \_ 2 0-Modell. Die Anzahl der Texturkoordinaten bleibt jedoch auf acht beschränkt. Der Zustand der Texturstufe ist Oberflächen, Koordinatensätzen, Vertexverarbeitung und Pixelverarbeitung zugeordnet. Um diese Unterschiede zur Kompilierzeit zu verwalten, wurde [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) in zwei Methoden unterteilt:

-   IDirect3DDevice9::SetTextureStageState wird weiterhin für den Texturkoordinatenzustand verwendet, z. B. Wrapmodi und Texturkoordinatengenerierung.
-   [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) wurde hinzugefügt und wird jetzt zum Filtern, Kacheln, Klammern, MIPLOD usw. verwendet. Dies funktioniert für bis zu 16 Sampler.

### <a name="settexturestagestate-changes"></a>SetTextureStageState-Änderungen

IDirect3DDevice9::SetTextureStageState legt jetzt die folgenden Zustände fest:

-   Der Verarbeitungsstatus des Funktionsvertex wurde korrigiert. Dieser Zustand steuert die Bearbeitung der Texturkoordinaten D3DTSS \_ TEXTURETRANSFORMFLAGS und D3DTSS \_ TEXCOORDINDEX. Bis zu acht davon können festgelegt werden (da immer acht Texturkoordinaten unterstützt werden). D3DTSS \_ TEXCOORDINDEX ist ein fester Funktionsvertexverarbeitungszustand. Wenn ein programmierbarer Vertex-Shader verwendet wird, wird dieser Zustand ignoriert.
-   Der Zustand des Funktionspixel-Shaders wurde korrigiert (legacy TextureStageState).

    -   D3DTSS \_ ALPHAARG0
    -   D3DTSS \_ ALPHAARG1
    -   D3DTSS \_ ALPHAARG2
    -   D3DTSS \_ ALPHAOP
    -   D3DTSS \_ BUMPENVLOFFSET
    -   D3DTSS \_ BUMPENVLSCALE
    -   D3DTSS \_ BUMPENVMAT00
    -   D3DTSS \_ BUMPENVMAT01
    -   D3DTSS \_ BUMPENVMAT10
    -   D3DTSS \_ BUMPENVMAT11
    -   D3DTSS \_ COLORARG0
    -   D3DTSS \_ COLORARG1
    -   D3DTSS \_ COLORARG2
    -   D3DTSS \_ COLOROP
    -   D3DTSS \_ RESULTARG

    Die Anzahl der Pixel-Shaderzustände fester Funktionen, die festgelegt werden können, ist kleiner oder gleich der Zahl, die von MaxTextureBlendStages dargestellt wird.

Die Anzahl der für die Anwendung verfügbaren Texturs sampler wird durch die Pixel-Shaderversion bestimmt, wie in der folgenden Tabelle angegeben.



| Name                    | Number                                                         |
|-------------------------|----------------------------------------------------------------|
| ps \_ 1 \_ 1 bis ps \_ 1 \_ 3    | 4 Texturs samplers                                             |
| ps \_ 1 \_ 4                | 6 Texturs samplers                                             |
| ps \_ 2 \_ 0                | 16 Texturs samplers                                            |
| Feste Funktionspipeline | MaxTextureBlendStages/MaxSimultaneousTextures-Texturs samplers |



 

Geräte, die die Verschiebungszuordnung in Direct3D 9 unterstützen, unterstützen einen zusätzlichen Sampler (D3DDMAPSAMPLER), der die Verschiebungszuordnungen in der Mosaikeinheit abtast.

### <a name="setsamplerstate-changes"></a>SetSamplerState-Änderungen

IDirect3DDevice9::SetSamplerState legt den Samplerzustand fest (einschließlich des in der Mosaikeinheit verwendeten , um Verschiebungszuordnungen zu beproben). Diese wurden mit einem D3DSAMP-Präfix umbenannt, um die Fehlererkennung zur Kompilierzeit beim Portieren von \_ DirectX 8.x zu ermöglichen. Die Zustände umfassen:

-   D3DSAMP \_ ADDRESSU
-   D3DSAMP \_ ADDRESSV
-   D3DSAMP \_ ADDRESSW
-   D3DSAMP \_ BORDERCOLOR
-   D3DSAMP \_ MAGFILTER
-   D3DSAMP \_ MAXANISOTROPY
-   D3DSAMP \_ MAXMIPLEVEL
-   D3DSAMP \_ MINFILTER
-   D3DSAMP \_ MIPFILTER
-   D3DSAMP \_ MIPMAPLODBIAS

## <a name="vertex-declaration-changes"></a>Vertexdeklarationsänderungen

Scheitelpunktdeklarationen sind jetzt von der Vertex-Shadererstellung entkoppelt. Scheitelpunktdeklarationen verwenden jetzt eine Component Object Model -Schnittstelle (COM).

Für DirectX 8.x sind Vertexdeklarationen an Vertex-Shader gebunden.

-   Rufen Sie für die Feste Funktionspipeline [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) mit dem FVF-Code (Flexible Vertex format) des Scheitelpunktpuffers auf.
-   Rufen Sie für Vertexshader IDirect3DDevice9::SetVertexShader mit einem Handle für einen zuvor erstellten Vertexshader auf. Der Shader enthält eine Scheitelpunktdeklaration.

Für Direct3D 9 werden Scheitelpunktdeklarationen von Vertex-Shadern entkoppelt und können entweder mit der Pipeline für feste Funktionen oder mit Shadern verwendet werden.

-   Für die Feste Funktionspipeline ist es nicht notwendig, IDirect3DDevice9::SetVertexShader aufrufen. Wenn Sie jedoch zur Festen Funktionspipeline wechseln möchten und zuvor einen Vertexshader verwendet haben, rufen Sie IDirect3DDevice9::SetVertexShader(**NULL) auf.** Wenn dies erfolgt ist, müssen Sie weiterhin [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) aufrufen, um den FVF-Code zu deklarieren.
-   Wenn Sie Vertexshader verwenden, rufen Sie IDirect3DDevice9::SetVertexShader mit dem Vertexshaderobjekt auf. Rufen Sie außerdem IDirect3DDevice9::SetFVF auf, um eine Scheitelpunktdeklaration zu einrichten. Dabei werden die in der FVF impliziten Informationen verwendet. [**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) kann statt IDirect3DDevice9::SetFVF aufgerufen werden, da vertex-Deklarationen unterstützt werden, die nicht mit einer FVF ausgedrückt werden können.

## <a name="intervals-and-swapeffects-changes"></a>Intervalle und SwapEffects-Änderungen

Es wurden mehrere Änderungen vorgenommen, um dem Benutzer mehr Kontrolle über die Aktualisierungsrate des Monitors, die Präsentationsrate und den Frontpuffer im Vergleich zur Backpufferzeichnung zu geben. Dies sind:

-   Ein Austauscheffekt, D3DSWAPEFFECT COPY VSYNC, und eine \_ Präsentationsrate, \_ D3DPRESENT \_ RATE \_ UNLIMITED, wurden entfernt.
-   Umbenannte D3DPRESENT-PARAMETER. \_ FullScreen \_ PresentationInterval in PresentationIntervals.
-   D3DPRESENT INTERVAL IMMEDIATE wurde hinzugefügt, was bedeutet, dass die \_ Präsentation nicht mit der \_ vertikalen Synchronisierung synchronisiert wird. Wie in DirectX 8.x ist D3DPRESENT INTERVAL DEFAULT als 0 (null) definiert und \_ \_ entspricht D3DPRESENT \_ INTERVAL \_ ONE. D3DPRESENT \_ INTERVAL DEFAULT ist eine Vereinfachung für die \_ Initialisierung von D3DPRESENT \_ PARAMETERS auf 0 (null).

Eine ausführliche Erläuterung der unterstützten Modi und Intervalle finden Sie unter D3DPRESENT.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 9-Grafiken](dx9-graphics.md)
</dt> </dl>

 

 
