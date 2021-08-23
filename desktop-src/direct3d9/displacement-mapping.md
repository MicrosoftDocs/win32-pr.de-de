---
description: Verschiebungszuordnungen ähneln Texturzuordnungen, aber die Vertex-Engine greift darauf zu.
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

Verschiebungszuordnungen ähneln Texturzuordnungen, aber die Vertex-Engine greift darauf zu.

## <a name="block-diagram"></a>Blockdiagramm

Eine zusätzliche Samplerphase ist im frühen Teil der Scheitelpunktpipe vorhanden, wie im folgenden Diagramm dargestellt, das eine Verschiebungskarte abtasten kann, um Vertexverschiebungensdaten bereitzustellen.

![Diagramm der Samplerphase in der Scheitelpunktpipe](images/tessellatordx9.png)

Der Zustand des Verschiebungszuordnungs-Samplers kann vom [**SetSamplerState**](/windows/desktop/api) mithilfe der Stufennummer 256 festgelegt werden. Dies ist eine neue Phasennummer. Die Verschiebungszuordnungstextur wird durch [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)festgelegt.

Die Karte kann vorsampelt werden oder nicht. Dies bedeutet, dass sie so sortiert werden kann, dass die Suche nach den Verschiebungswerten ohne Filterung ermöglicht wird.

-   Verschiebungszuordnungen sind analog zu Texturzuordnungen, aber der Zugriff erfolgt über die Scheitelpunkt-Engine.
-   Im frühen Teil der Scheitelpunktpipe ist eine zusätzliche Samplerphase vorhanden, die eine Verschiebungskarte abtasten kann. Auf diese Phase wird von der üblichen SetSamplerState-API zugegriffen, aber die Stufennummer ist D3DDMAPSAMPLER = 256.
-   Der Zustand des Verschiebungszuordnungs-Samplers kann durch SetSamplerState(D3DDMAPSAMPLER, ...) festgelegt werden. Api.
-   Die Verschiebungszuordnungstextur wird von der SetTexture(D3DDMAPSAMPLER, texture)-API festgelegt.
-   Die Karte kann vorab als Stichprobe entnommen werden oder nicht. Dies bedeutet, dass sie auf eine bestimmte Weise sortiert werden kann, die die Suche nach den Verschiebungswerten ohne Filterung ermöglicht.
-   Die Änderungen in der Deklarationsstruktur ermöglichen die Angabe der Texturkoordinate, die zum Suchen der Texturkarte verwendet wird. Beispiel: Stream0, Offset, FLOAT2, LOOKUP, \_ Versatzwert. Dies weist den Mosaikator an, den 2D-Gleitkommavektor in stream0 an einem bestimmten Offset als Texturkoordinate zu verwenden, um die Verschiebungskarte zu suchen und ihr die Verwendungssemantik des Werts \_ "Versatzwert" zuzuordnen. Die Vertex-Shaderdeklaration enthält eine Zeile ähnlich {dcl \_ texture0, v0}, die angibt, dass die Textur0-Semantik dem v0-Eingaberegister zugeordnet werden soll. Der gesuchte Verschiebungswert wird in das Eingaberegister v0 kopiert.
-   Es gibt einen besonderen Typ der Verschiebungszuordnung, wenn die Texturkarte vorab entnommen wird. Der sequenzielle Index der generierten Scheitelpunkte wird als Texturkoordinate für eine Texturkarte verwendet. Beispiel: 0,0,(D3DDECLTYPE)0,D3DDECLMETHOD \_ LOOKUPPRESAMPLED, Usage, UsageIndex.
-   Die Ausgabe der Suche ist 4 Gleitkommazahl.
-   Die Zuordnung von Verschiebungen wird nur mit N-Patches unterstützt.
-   Treiber müssen D3DDMAPSAMPLER in SetTextureStageState ignorieren, wenn sie keine Verschiebungszuordnungen verarbeiten.
-   Der \_ D3DTEXF-ANISOTROPE Filtermodus wird nicht unterstützt.
-   Wenn D3DSAMP \_ MIPFILTER im Sampling für die Verschiebungszuordnung nicht D3DTEXF \_ NONE ist, wird die Detailebene wie folgt berechnet (Beachten Sie, dass der adaptive Mosaikzustand auch dann verwendet wird, wenn D3DRS \_ ENABLEADAPTIVETESSELLATION **FALSE** ist): Tmax = Renderzustand D3DRS \_ MAXTESSELLATIONLEVEL
-   Berechnen Sie den Mosaikgrad Te für ein Scheitelpunkt vi: (Xi,Stufen, Zi) auf die gleiche Weise wie im Abschnitt "Adaptive Mosaik" beschrieben. Detailebene L = log2(Tmax) - log2 (Te).
-   Texturfilterungs- und Samplingvorgänge folgen den gleichen Regeln wie die Pixelpipeline (LOD-Verzerrung (Level of Detail) wird angewendet usw.).
-   Nicht alle Formate können als Verschiebungszuordnungen verwendet werden, sondern nur diejenigen, die D3DUSAGE \_ DMAP unterstützen. Die Anwendung kann dies mit checkDeviceFormat [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)abfragen.
-   D3DUSAGE \_ DMAP muss in [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) angegeben werden, um den Treiber darüber zu informieren, dass diese Textur als Verschiebungskarte verwendet werden soll.
-   D3DUSAGE \_ DMAP kann nur mit Texturen verwendet werden. Sie kann nicht mit Cubezuordnungen oder Volumes verwendet werden.
-   Texturen und Renderziele, die mit D3DUSAGE DMAP erstellt \_ wurden, können in regulären Samplerstufen und als Renderziele festgelegt werden.
-   Die Renderzustände zum Festlegen des Umbruchmodus für die Texturkoordinaten werden bei der Verschiebungszuordnung ignoriert. Im Allgemeinen gibt es keine Umbruchmodi für die Mosaik-Engine.
-   Ein Verschiebungszuordnungs-Sampler weist das gleiche Verhalten wie die Pixeltextur-Sampler auf. Wenn eine Textur mit weniger als vier Kanälen (z. B. R32f) gesucht wird, werden die gesuchten Werte an die entsprechenden Kanäle des Zielregisters (das Vertex-Shadereingaberegister mit der \_ Beispielsemantik markiert), während die anderen Kanäle standardmäßig (1, 1, 1) sind. Bei der Suche wird D3DFMT \_ L8 in die R-, G-, B-Kanäle übertragen, und A ist standardmäßig auf 1 eingestellt. Der Referenzraster enthält die vollständigen Implementierungsdetails.

## <a name="pre-sampled-displacement-mapping"></a>Zuordnung vorab entnommener Verschiebungen

-   Der neue Samplerzustand wird eingeführt: D3DSAMP \_ DMAPOFFSET (DWORD) – Offset (in Scheitelpunkten) in einer vorab entnommenen Verschiebungskarte.
-   Es wird eine neue Deklarationsmethode eingeführt: D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   Das adaptive Mosaik sollte deaktiviert werden.
-   Texturfiltereinstellungen werden ignoriert. Die Punktstichprobe ist abgeschlossen. Der mip-Texturfilter wird als D3DTEXF \_ NONE angenommen. Alle anderen Texturfiltermodi werden als D3DTEXF \_ POINT angenommen.
-   Texturkoordinaten werden berechnet wie: U = (Index % TextureWidthInPixeles) / (float)(TextureWidthInPixeles) V = (Index / TextureWidthInPixeles) / (float)(TextureHeightInPixeles), wobei Index ein sequenzieller Index von generierten Scheitelpunkten plus TSS \[ D3DSAMP \_ DMAPOFFSET \] ist. Der sequenzielle Index wird am Anfang jedes Primitives auf 0 (null) festgelegt und nach dem Generieren eines Scheitelpunkts erhöht.

Dies sind die API-Änderungen, die die Zuordnung von Verschiebungen unterstützen.

-   Es wurde ein einzelnes Kanalformat hinzugefügt, D3DFMT \_ L16.
-   Ein neues Verwendungsflag, D3DUSAGE \_ DMAP.
-   Eine spezielle Texturphase, die verwendet wird, um eine Verschiebungszuordnungstextur D3DDMAPSAMPLER festzulegen.
-   Es wurden neue Hardwareobergrenzen hinzugefügt: D3DDEVCAPS2 \_ DMAPNPATCH und D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH. Siehe [D3DDEVCAPS2.](d3ddevcaps2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertexpipeline](vertex-pipeline.md)
</dt> </dl>

 

 
