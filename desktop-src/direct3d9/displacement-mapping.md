---
description: Verschiebungs Zuordnungen ähneln Textur Karten, aber der Vertex-Engine wird darauf zugreifen.
ms.assetid: d6f16ff2-5a66-48a3-82c4-523faaafa6ae
title: Verschiebungs Zuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b687583b0109223d8c2dac807425e235ddf280e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482078"
---
# <a name="displacement-mapping-direct3d-9"></a>Verschiebungs Zuordnung (Direct3D 9)

Verschiebungs Zuordnungen ähneln Textur Karten, aber der Vertex-Engine wird darauf zugreifen.

## <a name="block-diagram"></a>Block Diagramm

Eine zusätzliche Samplingphase ist im frühen Teil der vertexpipe vorhanden, wie im folgenden Diagramm gezeigt, das eine Verschiebungs Zuordnung zum Bereitstellen von Scheitelpunkt Verschiebungs Daten darstellen kann.

![Diagramm der Samplingphase in der Scheitelpunkt Pipe](images/tessellatordx9.png)

Der Status des Verschiebungs Karten Samplers kann von [**setsamplerstate**](/windows/desktop/api) mithilfe der Phasen Nummer 256 festgelegt werden. dabei handelt es sich um eine neue Stufen Nummer. Die Struktur der Verschiebungs Zuordnung wird von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)festgelegt.

Die Zuordnung kann vorab erstellt werden, d. h., Sie kann so angeordnet werden, dass die Suche nach den Verschiebungs Werten ohne Filterung ermöglicht wird.

-   Verschiebungs Zuordnungen entsprechen Textur Zuordnungen, auf die Vertex-Engine wird jedoch zugegriffen.
-   Eine zusätzliche Samplingphase ist im frühen Teil der vertexpipe vorhanden, die eine Verschiebungs Karte enthalten kann. Auf diese Stufe wird über die übliche setsamplerstate-API zugegriffen, aber die Stufen Nummer ist D3DDMAPSAMPLER = 256.
-   Der Status des Verschiebungs Karten Samplers kann durch setsamplerstate (D3DDMAPSAMPLER,...) festgelegt werden. Found.
-   Die Struktur der Verschiebungs Zuordnung wird von der SetTexture-API (D3DDMAPSAMPLER, Texture) festgelegt.
-   Die Zuordnung kann vorab abgetastet werden. Dies bedeutet, dass Sie auf eine bestimmte Weise angeordnet werden kann, die die Suche nach Verschiebungs Werten ohne Filterung ermöglicht.
-   Die Änderungen in der Deklarations Struktur ermöglichen die Angabe der Textur Koordinate, die verwendet wird, um die Textur Zuordnung zu suchen. Beispielsweise Stream0, Offset, FLOAT2, Lookup, Verschiebungs \_ Wert. Dadurch wird der Mosaik Dienst aufgefordert, den 2D-float-Vektor in stream0 an einem bestimmten Offset als Textur Koordinate zu verwenden, um die Verschiebungs Zuordnung zu suchen und die \_ Verwendungs Semantik der Verschiebungs Werte zuzuordnen. Die Vertex-Shader-Deklaration enthält eine Zeile ähnlich "{DCL \_ Texture0, v0}", die angibt, dass die Texture0-Semantik dem Register "v0 Input" zugeordnet werden soll. Der ersuchte Verschiebungs Wert wird in das Eingabe Register "v0" kopiert.
-   Es gibt eine besondere Art von Verschiebungs Zuordnung, wenn die Textur Zuordnung vorab abgetippt wird. Ein sequenzieller Index generierter Vertices wird als Textur Koordinate für eine Textur Zuordnung verwendet. Beispiel: 0, 0, (D3DDECLTYPE) 0, D3DDECLMETHOD \_ lookuppresampling, Usage, US-Index.
-   Die Ausgabe der Suche ist 4 Gleit Komma Zahlen.
-   Die Verschiebungs Zuordnung wird nur mit N-Patches unterstützt.
-   Treiber müssen D3DDMAPSAMPLER in settexturestagestate ignorieren, wenn Sie keine Verschiebungs Zuordnungen verarbeiten.
-   Der D3DTEXF \_ anisotrope-Filter Modus wird nicht unterstützt.
-   Wenn D3DSAMP \_ MipFilter im Verschiebungs Karten-Sampler nicht D3DTEXF \_ None ist, wird die Detailebene wie folgt berechnet (Beachten Sie, dass der Adaptive Mosaik Zustand auch dann verwendet wird, wenn D3DRS \_ enableadaptivetesellation **false** ist): TMAX = Rendering State D3DRS \_ maxtmeellationlevel.
-   Compute-Mosaik Ebene für einen Vertex VI: (XI, Yi, Zi) auf die gleiche Weise wie im Abschnitt "Adaptive Mosaik" beschrieben. Detailebene L = log2 (TMAX)-log2 (TE).
-   Bei der Textur Filterung und bei Samplings werden die gleichen Regeln befolgt wie für die Pixel Pipeline (detailsgrads (Grad)).
-   Nicht alle Formate können als Verschiebungs Zuordnungen verwendet werden, aber nur diejenigen, die die D3DUSAGE- \_ dmap unterstützen. Die Anwendung kann das CheckDeviceFormat mit CheckDeviceFormat [**Abfragen.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
-   D3DUSAGE \_ dmap muss in " [**kreatetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) " angegeben werden, um den Treiber zu benachrichtigen, dass diese Textur als Verschiebungs Zuordnung verwendet werden soll.
-   D3DUSAGE \_ dmap kann nur mit Texturen verwendet werden. Sie kann nicht mit Cubemaps oder Volumes verwendet werden.
-   Texturen und Renderziele, die mit D3DUSAGE dmap erstellt wurden, \_ können in regulären samplingstufen und als Renderziele festgelegt werden
-   Die renderzustände, um den Umbruch Modus für die Texturkoordinaten festzulegen, werden bei der Verschiebungs Zuordnung ignoriert. Im Allgemeinen gibt es keine Wrap-Modi für die Mosaik-Engine.
-   Ein Verschiebungs kartensampler weist ein Verhalten auf, das mit dem des Pixel Textur Samplers identisch ist. Wenn eine Textur mit weniger als vier Kanälen (z. b. R32f) gesucht wird, werden die nach-oben-Werte in den entsprechenden Kanälen des Ziel Registers (dem Vertex-Shader-Eingabe Register, das mit der \_ Beispiel Semantik gekennzeichnet ist) angezeigt, während die anderen Kanäle standardmäßig auf (1, 1, 1) eingestellt sind. Bei der Suche wird D3DFMT \_ L8 in die R-, G-, B-Kanäle und standardmäßig auf 1 übertragen. Der Verweis Raster verfügt über die vollständigen Implementierungsdetails.

## <a name="pre-sampled-displacement-mapping"></a>Verschiebungs Zuordnung vor Stichproben

-   Der neue samplerstatus wurde eingeführt: D3DSAMP \_ dmapoffset (DWORD)-Offset (in Scheitel Punkten) in einer vorab komprimierten Verschiebungs Zuordnung.
-   Die neue Deklarations Methode wurde eingeführt: D3DDECLMETHOD \_ lookuppresampling.
-   Das Adaptive Mosaik sollte deaktiviert werden.
-   Textur Filtereinstellungen werden ignoriert. Die Punkt Stichprobe ist abgeschlossen. Es wird angenommen, dass der MIP-Textur Filter D3DTEXF \_ None ist. Alle anderen Textur Filtermodi werden als D3DTEXF Punkt angenommen \_ .
-   Texturkoordinaten werden wie folgt berechnet: U = (Index% texturewidthinpixeles)/(float) (texturewidthinpixeles) V = (Index/texturewidthinpixeles)/(float) (textureturetinpixeles), wobei Index ein sequenzieller Index generierter Vertices Plus TSS \[ D3DSAMP \_ dmapoffset ist \] . Der sequenzielle Index wird am Anfang der einzelnen primitiven auf NULL festgelegt und nach der Generierung eines Scheitel Punkts erweitert.

Dies sind die API-Änderungen, die die Verschiebungs Zuordnung unterstützen.

-   Es wurde ein einzelnes Kanal Format hinzugefügt, D3DFMT \_ L16.
-   Ein neues nutzungsflag, D3DUSAGE \_ dmap.
-   Eine spezielle Textur Phase, mit der eine Verschiebungs Karten Textur, D3DDMAPSAMPLER, festgelegt wird.
-   Es wurden neue Hardware Obergrenzen hinzugefügt, D3DDEVCAPS2 \_ dmapnpatch und D3DDEVCAPS2 \_ presampleddmapnpatch. Siehe [D3DDEVCAPS2](d3ddevcaps2.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunkt Pipeline](vertex-pipeline.md)
</dt> </dl>

 

 
