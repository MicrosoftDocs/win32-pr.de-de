---
description: Die folgenden Features wurden in Microsoft Direct3D 9 geändert. Wenn Sie diese Features verwenden, sehen Sie sich die unten aufgeführten Änderungen an, um Ihre Anwendung auf Direct3D 9 zu portieren.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Wandeln in Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becdb878ad462bfc0157fb15b3c9c1ef2ba158dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346858"
---
# <a name="converting-to-direct3d-9"></a>Wandeln in Direct3D 9

Die folgenden Features wurden in Microsoft Direct3D 9 geändert. Wenn Sie diese Features verwenden, sehen Sie sich die unten aufgeführten Änderungen an, um Ihre Anwendung auf Direct3D 9 zu portieren.

-   [Basevertexindex-Änderungen](#basevertexindex-changes)
-   ["Kreateimagesurface"-Änderungen](#createimagesurface-changes)
-   [D3DENUM \_ keine \_ Änderungen an WHQL- \_ Ebene](/windows)
-   [Erstellen von Ressourcen Änderungen](#create-resource-changes)
-   [Enumadaptermodes-Änderungen](#enumadaptermodes-changes)
-   [Get/SetStreamSource- \_ Änderungen](#getsetstreamsource-changes)
-   [Qualitätsänderungen bei der Multisampling](#multisampling-quality-changes)
-   [Resourcemanagerverwerdbytes-Änderungen](#resourcemanagerdiscardbytes-changes)
-   [Setsoftwarevertexprocessing-Änderungen](#setsoftwarevertexprocessing-changes)
-   [Textursampler-Änderungen](#texture-sampler-changes)
-   [Vertex-Deklarations Änderungen](#vertex-declaration-changes)
-   [Intervalle \_ und \_ austauschen von \_ Änderungen](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a>Basevertexindex-Änderungen

In DirectX 8. x erforderte IDirect3DDevice8:: setindexes einen Zeiger auf den Index Puffer und einen basevertexindex für die Anfangsposition im Vertex-Puffer. Eine Anwendung, die unterschiedliche Objekte in den Vertex-Puffer unterteilt, musste den Index Puffer wechseln (oder IDirect3DDevice8:: setindexes aufrufen), bevor IDirect3DDevice8::D rawindexedprimitiv aufgerufen wird.

In Direct3D 9 wurde die Anfangsposition im Vertex-Puffer *basevertexindex* nach IDirect3DDevice9::D rawindexedprimitiv verschoben, und der Datentyp des Datentyps wurde von DWORD in int geändert.


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



## <a name="createimagesurface-changes"></a>"Kreateimagesurface"-Änderungen

IDirect3DDevice8:: kreateimagesurface wurde in " [**kreateoffscreenplainsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)" umbenannt. Ein zusätzlicher Parameter, der einen D3DPOOL-Typ annimmt, wurde hinzugefügt. D3DPOOL \_ Scratch gibt eine Oberfläche mit identischen Merkmalen für eine Oberfläche zurück, die von IDirect3DDevice8:: kreateimagesurface erstellt wurde. D3DPOOL \_ Default ist der geeignete Pool für die Verwendung mit [**stretchrect**](/windows/desktop/api) und [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).

## <a name="d3denum_no_whql_level-changes"></a>D3DENUM \_ keine \_ Änderungen an WHQL- \_ Ebene

Anwendungen müssen nun explizit Microsoft Windows Hardware Quality Labs (WHQL) anfordern, da die Antwort relativ lange dauert (einige Sekunden). D3DENUM es wurde \_ keine \_ WHQL \_ -Ebene entfernt, und die D3DENUM \_ WHQL- \_ Ebene wurde hinzugefügt.

## <a name="create-resource-changes"></a>Erstellen von Ressourcen Änderungen

Ein Handle wurde mehreren Methoden hinzugefügt und sollte auf **null** festgelegt werden. Folgende Methoden sind betroffen:

-   [**"Kreatetexture"**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**"Kreatevolumetexture"**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [**"Kreatecubetexture"**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**"Kreatevertexbuffer"**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [**"Kreateingedexbuffer"**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [**"Kreaterendertarget"**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [**"Kreatedepthstencilsurface"**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**"Kreateoffscreenplainsurface"**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a>Enumadaptermodes-Änderungen

[**Enumadaptermodes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) nimmt nun eine D3DFORMAT-Datei an.


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



Das Format unterstützt eine erweiternde Gruppe von Anzeigemodi. Um Anwendungen vor dem Auflisten von Formaten zu schützen, die beim Versand der Anwendung nicht erfunden wurden, muss die Anwendung Direct3D das Format für die Anzeigemodi angeben, die aufgelistet werden sollen. Das resultierende Array der Anzeigemodi unterscheidet sich nur durch die Breite, die Höhe und die Aktualisierungsrate.

Die Anwendung gibt ein Pixel Format an, und die Enumeration ist auf die Anzeigemodi beschränkt, die exakt mit dem Format übereinstimmen. Im folgenden finden Sie eine Liste der zulässigen Formate:

-   D3DFMT \_ A1R5G5B5
-   D3DFMT \_ A2B10G10R10
-   D3DFMT \_ A8R8G8B8
-   D3DFMT \_ R5G6B5
-   D3DFMT \_ X1R5G5B5
-   D3DFMT \_ X8R8G8B8

Die Enumeration ist äquivalent zu Alpha-und nonalpha-Versionen desselben Formats. Das zurückgegebene Format wird immer mit dem von der Anwendung bereitgestellten Format ausgefüllt.

Diese Methode behandelt 565 und 555 als gleichwertig und gibt die richtige Version im-Format zurück. Der Unterschied wird nur wiedergegeben, wenn die Anwendung den Hintergrund Puffer sperrt, und es gibt ein explizites Flag, das von der Anwendung festgelegt werden muss, um dies zu erreichen.

## <a name="getsetstreamsource-changes"></a>Get/SetStreamSource-Änderungen

Der [**getstreamsource**](/windows/desktop/api) -Methode und der [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) -Methode wurde ein Parameter hinzugefügt. Der Offset ist die Anzahl von Bytes zwischen dem Anfang des Streams und dem Anfang der Scheitelpunkt Daten. Der entsprechende Wert wird in „Bytes“ angegeben. Dadurch kann die Pipeline streamoffsets unterstützen. Informationen dazu, ob das Gerät streamoffsets unterstützt, finden Sie unter D3DDEVCAPS2 \_ Streamoffset.


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a>Qualitätsänderungen bei der Multisampling

Bisher gab es nur die D3DMULTISAMPLE \_ Type-Enumeration. Direct3D 9 behält diese Enumeration bei und fügt die Idee einer Qualitätsstufe für jedes Element der Enumeration hinzu. Die Qualitätsstufe gibt einen Kompromiss zwischen visueller Qualität und Leistung an, indem die Anzahl der hervor hefbaren Stichproben (im Sinne von D3DRS \_ multisamplemask) angegeben wird.

Eine Anwendung sollte auswählen, wie viele für Sie erforderliche Beispiele benötigt werden, und Sie sollten sich dann pqualitylevels ansehen. Wenn ungleich 0 (null) angegeben ist, gibt dieser Wert die Anzahl der Qualitätsstufen an, die die Anwendung über multisamplequality an die verschiedenen Erstellungs Funktionen übergeben kann. Da Treiber alle Ihre multibeispielschemas als Qualitäts Ebenen bei D3DMULTISAMPLE nicht \_ MASKABLE verfügbar machen, können Sie alle verfügbaren multisamplinggrad-Schemas über diesen Typ auflisten, wenn die Anwendung keine Beispiele maskieren muss.

Das D3DPRASTERCAPS \_ StretchBltMultisample Caps-Bit wurde eingestellt. Dieses Bit bedeutete, dass die multisamplinggrad-Methode Schreib Masken nicht unterstützte und zwischen [**BeginScene**](/windows/desktop/api) und [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene)nicht ein-und ausgeschaltet werden konnte. Solche nicht masretisierbaren Methoden werden nun über D3DMULTISAMPLE \_ Nonmaskable verfügbar gemacht.


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



Es gibt ein anderes Maximum für jede Anzahl von für das Paar baren Stichproben. Beispielsweise können D3DMULTISAMPLE \_ 4- \_ Beispiele drei Qualitätsstufen aufweisen, während D3DMULTISAMPLE- \_ \_ Stichproben möglicherweise nur eine Qualität aufweisen. Es gibt höchstens acht Qualitätsstufen für jede Anzahl von durchsuchbaren Beispielen (der Treiber ist nicht berechtigt, mehr auszudrücken). Die Qualität reicht von 0 (NULL \* ) bis (pqualitylevels-1).

## <a name="resourcemanagerdiscardbytes-changes"></a>Resourcemanagerverwerdbytes-Änderungen

Resourcemanagerverwerdbytes wurde durch IDirect3DDevice9:: evictmanagedresources ersetzt. Sie kann alle Ressourcen entfernen, sowohl Direct3D als auch Treiber Ressourcen.

Der Ressourcen-Manager wird jetzt bei der Erstellung einer Ressource (ob verwaltet oder nicht verwaltet) nicht ausgeführt, weil nicht genügend Videospeicher verfügbar ist. Der Manager wird automatisch aufgefordert, genügend Ressourcen freizugeben, damit die Erstellung erfolgreich durchgeführt werden kann. In DirectX 8,0 war dies kein automatisierter Prozess.

## <a name="setsoftwarevertexprocessing-changes"></a>Setsoftwarevertexprocessing-Änderungen

Eine Anwendung kann ein Gerät im gemischten Modus erstellen, um die Verarbeitung von Software-und Hardware Scheitel Punkten zu verwenden.

Um zwischen den beiden Scheitelpunkt Verarbeitungsmodi in DirectX 8. x zu wechseln, wird IDirect3DDevice8:: Server State aufgerufen. Dies wurde durch [**setsoftwarevertexprocessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) ersetzt, um Probleme zu vereinfachen, die durch Zustands Blöcke verursacht wurden. Diese neue Methode wird nicht von Zustands Blöcken aufgezeichnet.

## <a name="texture-sampler-changes"></a>Textursampler-Änderungen

Direct3D 9 unterstützt bis zu sechzehn Textur Oberflächen in einem Durchlauf mithilfe des Pixels-Shader 2 \_ 0-Modells. die Anzahl der Texturkoordinaten bleibt jedoch auf acht beschränkt. Der Textur Stufen Zustand ist mit Oberflächen, Koordinaten Sätzen, Vertexverarbeitung und Pixel Verarbeitung verknüpft. Um diese Unterschiede zur Kompilierzeit zu verwalten, wurde [**settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) in zwei Methoden unterteilt:

-   IDirect3DDevice9:: settexturestagestate wird weiterhin für den Texturkoordinaten Zustand verwendet, wie z. b. Umbruch Modi und Texturkoordinaten Generierung.
-   " [**Setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) " wurde hinzugefügt und wird jetzt zum Filtern, ticken, spannen, miplod usw. verwendet. Dies funktioniert für bis zu sechzehn samplz.

### <a name="settexturestagestate-changes"></a>Settexturestagestate-Änderungen

IDirect3DDevice9:: settexturestagestate legt nun die folgenden Zustände fest:

-   Verarbeitungs Status des Scheitelpunkt Status der Funktion. Dieser Zustand steuert die Bearbeitung von Texturkoordinaten D3DTSS \_ texturetransformflags und D3DTSS \_ texcoordindex. Es können bis zu acht von jedem festgelegt werden (da acht Texturkoordinaten immer unterstützt werden). D3DTSS \_ texcoordindex ist ein Status der Vertex-Verarbeitung fester Funktionen. Wenn ein programmierbarer Vertex-Shader verwendet wird, wird dieser Zustand ignoriert.
-   Fester funktionspixelshader-Zustand (Legacy texturestagestate).

    -   D3DTSS \_ ALPHAARG0
    -   D3DTSS \_ ALPHAARG1
    -   D3DTSS \_ ALPHAARG2
    -   D3DTSS \_ alphaop
    -   D3DTSS \_ bumpenvloffset
    -   D3DTSS \_ bumpendvlscale
    -   D3DTSS \_ BUMPENVMAT00
    -   D3DTSS \_ BUMPENVMAT01
    -   D3DTSS \_ BUMPENVMAT10
    -   D3DTSS \_ BUMPENVMAT11
    -   D3DTSS \_ COLORARG0
    -   D3DTSS \_ COLORARG1
    -   D3DTSS \_ COLORARG2
    -   D3DTSS \_ colorop
    -   D3DTSS \_ resultarg

    Die Anzahl der festzulegenden Pixel-Shader-Zustände fester Funktionen ist kleiner oder gleich der durch MaxTextureBlendStages dargestellten Zahl.

Die Anzahl der für die Anwendung verfügbaren Textur Samplern wird durch die Pixel-Shader-Version bestimmt, wie in der folgenden Tabelle angegeben.



| Name                    | Number                                                         |
|-------------------------|----------------------------------------------------------------|
| PS \_ 1 1 \_ bis PS \_ 1 \_ 3    | vier Textur-Samplern                                             |
| PS \_ 1 \_ 4                | 6 Textur-Samplern                                             |
| PS \_ 2 \_ 0                | 16 Textur-Samplern                                            |
| Fixed-Funktions Pipeline | MaxTextureBlendStages/maxdie oustextures Textur-Samplern |



 

Geräte, die die Verschiebungs Zuordnung in Direct3D 9 unterstützen, unterstützen einen zusätzlichen Sampler (D3DDMAPSAMPLER), der die Verschiebungs Zuordnungen in der Mosaik Einheit abbildet.

### <a name="setsamplerstate-changes"></a>Setsamplerstate-Änderungen

IDirect3DDevice9:: setsamplerstate legt den samplerstatus fest (einschließlich der in der Mosaik Einheit verwendeten Beispiel Verschiebungs Karten). Diese wurden mit einem D3DSAMP- \_ Präfix umbenannt, um die Kompilierzeit-Fehlererkennung beim Portieren aus DirectX 8. x zu aktivieren. Die Zustände umfassen Folgendes:

-   D3DSAMP \_ adressu
-   D3DSAMP \_ adressssv
-   D3DSAMP \_ AddressW
-   D3DSAMP \_ BorderColor
-   D3DSAMP- \_ MagFilter
-   D3DSAMP \_ MaxAnisotropy
-   D3DSAMP \_ MaxMipLevel
-   D3DSAMP \_ MinFilter
-   D3DSAMP \_ MipFilter
-   D3DSAMP \_ mipmaplodbias

## <a name="vertex-declaration-changes"></a>Vertex-Deklarations Änderungen

Vertex-Deklarationen werden nun von der Vertex-Shader-Erstellung entkoppelt. Vertex-Deklarationen verwenden jetzt eine Component Object Model (com)-Schnittstelle.

Bei DirectX 8. x sind Scheitelpunkt Deklarationen an Scheitelpunkt-Shader gebunden.

-   Bei der Fixed-Funktions Pipeline wird [**setvertexshader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) mit dem Code des flexiblen Scheitelpunkt Formats (FVF) des Scheitelpunkt Puffers aufgerufen.
-   Rufen Sie für Vertex-Shader IDirect3DDevice9:: setvertexshader mit einem Handle für einen zuvor erstellten Scheitelpunkt-Shader auf. Der Shader enthält eine Scheitelpunkt Deklaration.

Bei Direct3D 9 sind Scheitelpunkt Deklarationen von Vertex-Shadern entkoppelt und können mit der Fixed-Funktions Pipeline oder mit Shadern verwendet werden.

-   Bei der Fixed-Funktions Pipeline muss IDirect3DDevice9:: setvertexshader nicht aufgerufen werden. Wenn Sie jedoch zur Fixed-Funktions Pipeline wechseln und zuvor einen Vertex-Shader verwendet haben, aufrufen Sie IDirect3DDevice9:: setvertexshader (**null**). Wenn dies der Fall ist, müssen Sie auch [**setfvf**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) aufrufen, um den FVF-Code zu deklarieren.
-   Beim Verwenden von Vertex-Shadern wird IDirect3DDevice9:: setvertexshader mit dem Vertex-Shader-Objekt aufgerufen. Außerdem müssen Sie IDirect3DDevice9:: setfvf aufrufen, um eine Scheitelpunkt Deklaration einzurichten. Dabei werden die Informationen verwendet, die in der "f" implizit sind. [**Setvertexdeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) kann anstelle von IDirect3DDevice9:: setfvf aufgerufen werden, da es Scheitelpunkt Deklarationen unterstützt, die nicht mit einem FVF ausgedrückt werden können.

## <a name="intervals-and-swapeffects-changes"></a>Intervalle und Austauschen von Änderungen

Es wurden mehrere Änderungen vorgenommen, um dem Benutzer eine bessere Kontrolle über die Aktualisierungsrate des Monitors, die Präsentations Rate und den Vorder-und Hintergrund Puffer zu erhalten. Dies sind:

-   Ein Auslagerungs Effekt, D3DSWAPEFFECT \_ Copy \_ VSYNC und eine Präsentations Rate, D3DPRESENT \_ Rate \_ Unlimited, wurde entfernt.
-   Umbenannte D3DPRESENT- \_ Parameter. Vollbild- \_ presentationinterval zu presentationinterval.
-   D3DPRESENT \_ Interval \_ wurde sofort hinzugefügt, was bedeutet, dass die Präsentation nicht mit der vertikalen Synchronisierung synchronisiert wird. Wie in DirectX 8. x ist D3DPRESENT \_ Interval \_ Default als 0 (null) definiert und entspricht D3DPRESENT \_ Interval \_ 1. D3DPRESENT \_ Interval \_ Default ist eine einfache Initialisierung von D3DPRESENT- \_ Parametern mit 0 (null).

Eine ausführliche Erläuterung der Modi und der unterstützten Intervalle finden Sie unter D3DPRESENT.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 9-Grafiken](dx9-graphics.md)
</dt> </dl>

 

 
