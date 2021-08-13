---
description: Verschiebungszuordnungen ähneln Texturzuordnungen, werden jedoch von der Scheitelpunkt-Engine aufgerufen.
ms.assetid: d6f16ff2-5a66-48a3-82c4-523faaafa6ae
title: Verschiebungszuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87b559c2c4758b773c48c0b556b6d61af54549f1b30e5c2693a24c4c27856c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523764"
---
# <a name="displacement-mapping-direct3d-9"></a>Verschiebungszuordnung (Direct3D 9)

Verschiebungszuordnungen ähneln Texturzuordnungen, werden jedoch von der Scheitelpunkt-Engine aufgerufen.

## <a name="block-diagram"></a>Blockdiagramm

Im frühen Teil der Scheitelpunktpipe ist eine zusätzliche Samplerphase vorhanden, wie im folgenden Diagramm dargestellt, mit der eine Verschiebungszuordnung entnommen werden kann, um Vertexverschiebungsdaten zu liefern.

![Diagramm der Samplerphase in der Scheitelpunktpipe](images/tessellatordx9.png)

Der Zustand des Verschiebungszuordnungs-Samplers kann von [**SetSamplerState**](/windows/desktop/api) mit der Phase 256 festgelegt werden, bei der es sich um eine neue Phasennummer handelt. Die Verschiebungszuordnungstextur wird von [**SetTexture festgelegt.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)

Die Karte kann vorab vorgefertigt werden, was bedeutet, dass sie so geordnet werden kann, dass die Verschiebungswerte ohne Filterung nachschlagen können.

-   Verschiebungszuordnungen sind analog zu Texturzuordnungen, aber der Zugriff erfolgt über die Scheitelpunkt-Engine.
-   Im frühen Teil der Scheitelpunktpipe ist eine zusätzliche Samplerphase vorhanden, mit der eine Verschiebungskarte entnommen werden kann. Auf diese Phase wird von der üblichen SetSamplerState-API zugegriffen, aber die Phasennummer ist D3DDMAPSAMPLER = 256.
-   Der Zustand des Verschiebungszuordnungs-Samplers kann durch SetSamplerState(D3DDMAPSAMPLER, ...) festgelegt werden. Api.
-   Die Verschiebungszuordnungstextur wird von der SetTexture(D3DDMAPSAMPLER, texture)-API festgelegt.
-   Für die Zuordnung kann eine Vorabstichprobe verwendet werden. Dies bedeutet, dass sie auf eine bestimmte Weise geordnet werden kann, die das Suchen der Verschiebungswerte ohne Filterung ermöglicht.
-   Die Änderungen in der Deklarationsstruktur ermöglichen die Angabe der Texturkoordinate, die zum Suchen der Texturkarte verwendet wird. Beispiel: Stream0, Offset, FLOAT2, LOOKUP, \_ Verschiebungswert. Dies weist den Mosaikator an, den 2D-Gleitkommavektor in stream0 an einem bestimmten Offset als Texturkoordinate zu verwenden, um die Verschiebungszuordnung nachschlagen und ihr die Semantik der Verschiebungswertverwendung zu \_ zuordnen. Die Vertex-Shaderdeklaration würde eine Zeile ähnlich {dcl texture0, v0} enthalten, die angibt, dass die Texture0-Semantik dem \_ v0-Eingaberegister zugeordnet werden soll. Der nach durchdrungene Verschiebungswert wird in das Eingaberegister v0 kopiert.
-   Es gibt eine besondere Art von Verschiebungszuordnung, wenn die Texturzuordnung vorab entnommen wird. Der sequenzielle Index generierter Scheitelungen wird als Texturkoordinate für eine Texturkarte verwendet. Beispiel: 0,0,(D3DDECLTYPE)0,D3DDECLMETHOD \_ LOOKUPPRESAMPLED, Usage, UsageIndex.
-   Die Ausgabe der Suche ist 4 gleitkomma.
-   Die Zuordnung von Verschiebungen wird nur mit N-Patches unterstützt.
-   Treiber müssen D3DDMAPSAMPLER in SetTextureStageState ignorieren, wenn sie keine Verschiebungszuordnungen verarbeiten.
-   Der D3DTEXF \_ ANISOTROPIC-Filtermodus wird nicht unterstützt.
-   Wenn D3DSAMP MIPFILTER im Verschiebungszuordnungs-Sampler nicht D3DTEXF NONE ist, wird die Detailebene wie folgt berechnet (beachten Sie, dass der adaptive Mosaikzustand auch dann verwendet wird, wenn \_ \_ D3DRS \_ ENABLEADAPTIVETESSELLATION **FALSE** ist): Tmax = Renderzustand D3DRS \_ MAXTESSELLATIONLEVEL
-   Compute tessellation level Te for a vertex Vi: (Xi, Soll, Zi) auf die gleiche Weise wie im Abschnitt "Adaptive Mosaik" beschrieben. Detailstufe L = log2(Tmax) - log2 (Te).
-   Texturfilterungs- und Samplingvorgänge folgen den gleichen Regeln wie die Pixelpipeline (LoD-Bias (Level of Detail) wird angewendet usw.).
-   Nicht alle Formate können als Verschiebungszuordnungen verwendet werden, sondern nur solche, die D3DUSAGE \_ DMAP unterstützen. Die Anwendung kann diese mit checkDeviceFormat [**CheckDeviceFormat abfragen.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
-   D3DUSAGE \_ DMAP muss in [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) angegeben werden, um den Treiber darüber zu informieren, dass diese Textur als Verschiebungszuordnung verwendet werden soll.
-   D3DUSAGE \_ DMAP kann nur mit Texturen verwendet werden. Sie kann nicht mit Cubezuordnungen oder Volumes verwendet werden.
-   Texturen und Renderziele, die mit D3DUSAGE DMAP erstellt wurden, können in regulären \_ Samplerphasen und als Renderziele festgelegt werden.
-   Die Renderzustände zum Festlegen des Umbruchmodus für die Texturkoordinaten werden in der Verschiebungszuordnung ignoriert. Im Allgemeinen gibt es keine Wrapmodi für die Mosaik-Engine.
-   Ein Verschiebungszuordnungs-Sampler hat das gleiche Verhalten wie die Pixeltextur-Sampler. Wenn eine Textur mit weniger als vier Kanälen (z. B. R32f) nachschlagen wird, werden die nachschlagenen Werte an die entsprechenden Kanäle des Zielregisters (das Mit der Beispielsemantik markierte Vertex-Shader-Eingaberegister) und die anderen Kanäle standardmäßig \_ (1, 1, 1) angezeigt. Bei der Suche wird D3DFMT L8 in die Kanäle R, G, B übertragen, und \_ A wird standardmäßig auf 1 festgelegt. Der Referenzraster verfügt über die vollständigen Implementierungsdetails.

## <a name="pre-sampled-displacement-mapping"></a>Zuordnung von Verschiebungen vor der Stichprobenentnahme

-   Neuer Samplerzustand wird eingeführt: D3DSAMP DMAPOFFSET (DWORD) – Offset (in Scheitelten) in einer vorab entnommenen \_ Verschiebungskarte.
-   Es wird eine neue Deklarationsmethode eingeführt: D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   Adaptives Mosaik sollte deaktiviert werden.
-   Texturfiltereinstellungen werden ignoriert. Die Punktstichproben werden durchgeführt. Es wird davon ausgegangen, dass der MIP-Texturfilter D3DTEXF \_ NONE ist. Alle anderen Texturfiltermodi werden als D3DTEXF \_ POINT angenommen.
-   Texturkoordinaten werden berechnet wie: U = (Index % TextureWidthInPixeles) / (float)(TextureWidthInPixeles) V = (Index /TextureWidthInPixeles) / (float)(TextureHeightInPixeles), wobei Index ein sequenzieller Index generierter Scheitelpunkte plus TSS \[ D3DSAMP \_ DMAPOFFSET \] ist. Der sequenzielle Index wird am Anfang jedes Primitiven auf 0 (null) festgelegt und erhöht, nachdem ein Scheitelpunkt generiert wurde.

Dies sind die API-Änderungen, die die Zuordnung von Verschiebungen unterstützen.

-   Ein hinzugefügtes Einzelkanalformat, D3DFMT \_ L16.
-   Ein neues Verwendungsflag, D3DUSAGE \_ DMAP.
-   Eine spezielle Texturstufe, die zum Festlegen einer Verschiebungszuordnungstextur verwendet wird, D3DDMAPSAMPLER.
-   Es wurden neue Hardware-Caps hinzugefügt: D3DDEVCAPS2 \_ DMAPNPATCH und D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH. Siehe [D3DDEVCAPS2](d3ddevcaps2.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertexpipeline](vertex-pipeline.md)
</dt> </dl>

 

 
