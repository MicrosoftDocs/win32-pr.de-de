---
description: In der Vertexpipeline der festen Funktion wendet die Verarbeitung der Scheitelpunkte in einem Scheitelpunktpuffer die aktuellen Transformationsmatrizen für das Gerät an.
ms.assetid: a882a5c5-b05e-4659-9040-92d3e2ccd89c
title: Vertexverarbeitung der Funktion korrigiert (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827a293a4fbd552327d93076de773aec90dbd895faf3c086f4794036978984fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988020"
---
# <a name="fixed-function-vertex-processing-direct3d-9"></a>Vertexverarbeitung der Funktion korrigiert (Direct3D 9)

In der Vertexpipeline der festen Funktion wendet die Verarbeitung der Scheitelpunkte in einem Scheitelpunktpuffer die aktuellen Transformationsmatrizen für das Gerät an. Vertexvorgänge wie Beleuchtung, Generieren von Clipflags und Aktualisieren von Erweiterungen können optional ebenfalls angewendet werden. Bei Verwendung der Vertexverarbeitung fester Funktionen wird das Ändern der Elemente im Zielvertexpuffer durch das [D3DPV \_ DONOTCOPYDATA-Flag](other-direct3d-constants.md) gesteuert. Dieses Flag gilt nur für die Vertexverarbeitung fester Funktionen. Die [**IDirect3DDevice9-Schnittstelle**](/windows/desktop/api) macht die [**IDirect3DDevice9::P rocessVertices-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) verfügbar, um Scheitelungen zu verarbeiten. Sie verarbeiten Scheitelpunkte von einem Vertex-Shader bis zum Satz von Eingabedatenströmen und generieren einen einzelnen Stream verleavter Vertexdaten zum Ziel-Scheitelpunktpuffer, indem Sie die **IDirect3DDevice9::P rocessVertices-Methode** aufrufen. Die -Methode akzeptiert fünf Parameter, die den Speicherort und die Menge der Scheitelpunkte beschreiben, auf die die Methode zielt, den Ziel-Scheitelpunktpuffer und die Verarbeitungsoptionen. Nach dem Aufruf enthält der Zielpuffer die verarbeiteten Scheitelpunktdaten.

Der erste, zweite und dritte Parameter, SrcStartIndex, DestIndex und VertexCount, spiegeln den Index des ersten zu ladenden Scheitelpunkts, den Index im Zielpuffer, in dem die Scheitelpunkte platziert werden, und die Gesamtzahl der Scheitelpunkte wider, die im Zielpuffer zu verarbeiten und zu platzieren sind. Der vierte Parameter pDestBuffer sollte auf die Adresse der [**IDirect3DVertexBuffer9-Schnittstelle**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) des Scheitelpunktpufferobjekts festgelegt werden, das die Quellvertices empfangen wird. Der SrcStartIndex-Parameter gibt den Index an, an dem die Methode mit der Verarbeitung von Scheiteltices beginnen soll.

Der letzte Parameter Flags bestimmt spezielle Verarbeitungsoptionen für die -Methode. Sie können diesen Parameter für die Standardvertexverarbeitung auf 0 oder in einigen Situationen auf [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) festlegen, um die Verarbeitung zu optimieren. Sie können auch den D3DPV DONOTCOPYDATA-Wert mit mindestens einem \_ [D3DLOCK-Wert](d3dlock.md) kombinieren, der für den Zielpuffer geeignet ist. Wenn Sie Flags auf 0 festlegen, werden Scheitelpunktkomponenten des Scheitelpunktformats des Scheitelpunktpuffers, die nicht vom Scheitelpunktvorgang betroffen sind, weiterhin aus dem Vertex-Shader kopiert oder auf 0 festgelegt. Bei Verwendung von D3DPV \_ DONOTCOPYDATA überschreibt [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) jedoch keine Farb- und Texturkoordinateninformationen im Zielpuffer, es sei denn, diese Daten werden von Direct3D generiert. Diffuse Farbe wird generiert, wenn die Beleuchtung aktiviert ist, d. b. D3DRS \_ LIGHTING ist auf TRUE **festgelegt.** Specular color is generated when lighting is enabled and specular is enabled, that is, D3DRS\_SPECULARENABLE and D3DRS\_LIGHTING are set to **TRUE**. Die Specular-Farbe wird auch generiert, wenn Einfärbung aktiviert ist. Texturkoordinaten werden generiert, wenn Texturtransformation oder Texturgenerierung aktiviert ist. **IDirect3DDevice9::P rocessVertices** verwendet die aktuellen Renderzustände, um zu bestimmen, welche Scheitelpunktverarbeitung erfolgen soll.

## <a name="fvf-usage-settings-for-destination-vertex-buffers"></a>FVF-Einstellungen für Ziel-Scheitelpunktpuffer

Die [**IDirect3DDevice9::P rocessVertices-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) erfordert bestimmte Einstellungen für [die D3DFVF](d3dfvf.md) des Zielvertexpuffers. Die FVF-Nutzungseinstellungen müssen mit den aktuellen Einstellungen für die Scheitelpunktverarbeitung kompatibel sein.

Für die Vertexverarbeitung fester Funktionen erfordert [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) die folgenden FVF-Einstellungen:

-   Der Positionstyp ist immer [D3DFVF \_ XYZRHW.](d3dfvf.md) Daher sind D3DFVF XYZ und \_ D3DFVF \_ XYZB1 bis D3DFVF \_ XYZB5 ungültig.
-   Die [Flags D3DFVF \_ NORMAL,](d3dfvf.md)D3DFVF RESERVED0 und \_ D3DFVF \_ RESERVED2 dürfen nicht festgelegt werden.
-   Das [DIFFUS-Flag \_ D3DFVF](d3dfvf.md) muss festgelegt werden, wenn ein OR-Vorgang der folgenden Bedingungen TRUE zurückgibt:
    -   Beleuchtung ist aktiviert. Das heißt, D3DRS \_ LIGHTING ist **TRUE.**
    -   Die Beleuchtung ist deaktiviert, die diffuse Farbe ist in den Eingabevertexstreams vorhanden, und [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) ist nicht festgelegt.
-   Das [ \_ SPECULAR-Flag D3DFVF](d3dfvf.md) muss festgelegt werden, wenn ein OR-Vorgang der folgenden Bedingungen TRUE zurückgibt:
    -   Die Beleuchtung ist aktiviert, und die Specular-Farbe ist aktiviert. D3DRS \_ SPECULARENABLE ist **true.**
    -   Die Beleuchtung ist deaktiviert, die Specularfarbe ist in den Eingabevertexstreams vorhanden, und [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) ist nicht festgelegt.
    -   Scheitelpunkt-Scheitelpunkt ist aktiviert. \_D3DRSSCHLUSSVERTEXMODE ist nicht auf D3DFOG \_ NONE festgelegt.

Darüber hinaus muss die Texturkoordinatenanzahl wie folgt festgelegt werden:

-   Wenn Texturtransformation und Texturgenerierung für alle aktiven Texturphasen deaktiviert sind und [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) nicht festgelegt ist, sind die Anzahl und der Typ der Ausgabetexturkoordinaten erforderlich, um mit denen der Texturkoordinaten der Eingabevertextextur überein stimmen. Wenn D3DPV DONOTCOPYDATA festgelegt ist und Texturtransformation und Texturgenerierung deaktiviert sind, werden die \_ Ausgabetexturkoordinaten ignoriert.
-   Wenn Texturtransformation oder Texturgenerierung für aktive Texturphasen aktiviert ist, muss der Ausgabevertex möglicherweise mehr Texturkoordinatensätze enthalten als der Eingabevertex. Dies liegt an der Verbreitung von Texturkoordinaten, die von Texturgenerierung generiert oder von Texturtransformationen abgeleitet werden. Beachten Sie, dass eine ähnliche Zunahme von Texturkoordinaten bei [**IDirect3DDevice9::D rawPrimitive-Aufrufen**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) auftritt, aber für den Anwendungsprogrammierer nicht sichtbar ist. In diesem Fall generiert Direct3D einen neuen Satz von Texturkoordinaten. Der neue Satz von Texturkoordinaten wird abgeleitet, indem die Texturstufen durchschritten und die Einstellungen für Texturgenerierung, Texturtransformation und Texturkoordinatenindex analysiert werden, um zu bestimmen, ob für diese Phase ein eindeutiger Satz von Texturkoordinaten erforderlich ist. Jedes Mal, wenn eine neue Gruppe erforderlich ist, wird sie in auf steigender Reihenfolge zugeordnet. Beachten Sie, dass die maximale und typische Anforderung eine Menge pro Phase ist, obwohl sie aufgrund der Gemeinsamen Nutzung nicht übersetzter Texturkoordinaten über D3DTSS \_ TEXCOORDINDEX geringer sein kann.

Daher wird für jede Texturphase ein neuer Satz von Texturkoordinaten generiert, wenn eine Textur an diese Phase gebunden ist und eine der folgenden Bedingungen zutrifft:

-   Die Texturgenerierung ist für diese Phase aktiviert.
-   Die Texturtransformation ist für diese Phase aktiviert.
-   Auf nicht übersetzte Eingabetexturkoordinaten wird zum ersten Mal über D3DTSS \_ TEXCOORDINDEX verwiesen.

Wenn Direct3D Texturkoordinaten generiert, muss die Anwendung die folgenden Aktionen ausführen:

1.  Verwenden Sie einen Ziel-Scheitelpunktpuffer mit der entsprechenden FVF-Nutzung.
2.  Programieren Sie den D3DTSS TEXCOORDINDEX der Texturphase entsprechend der Platzierung der nachverarbeiteten \_ Texturkoordinaten neu. Beachten Sie, dass die Neuprogrammierung der D3DTSS TEXCOORDINDEX-Einstellung auftritt, wenn der verarbeitete Scheitelpunktpuffer in nachfolgenden \_ [**IDirect3DDevice9::D rawPrimitive-**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) und [**IDirect3DDevice9::D rawIndexedPrimitive-Aufrufen**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) verwendet wird.

Schließlich muss die Texturkoordinatendimensionalität ([D3DFVF \_ TEX0](d3dfvf.md) bis D3DFVF \_ TEX8 ) wie folgt festgelegt werden:

-   Wenn für jeden Texturkoordinatensatz Texturtransformation und Texturgenerierung deaktiviert sind, muss die Ausgabetexturkoordinatendimensionalität mit der Eingabe übereinstimmen. Wenn die Texturtransformation aktiviert ist, muss die Ausgabedimensionalität mit der Anzahl übereinstimmen, die in den Einstellungen D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF COUNT3 oder \_ D3DTTFF COUNT4 definiert \_ ist. Wenn die Texturtransformation deaktiviert und die Texturgenerierung aktiviert ist, muss die Ausgabedimensionalität mit den Einstellungen für den Texturgenerierungsmodus übereinstimmen. derzeit generieren alle Modi drei Gleitkommawerte.

Wenn [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) aufgrund eines inkompatiblen FVF-Ziel-Scheitelpunktpuffers fehlschlägt, wird der erwartete Code in die Debugausgabe ausgegeben (nur Debugbuilds).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunktpuffer](vertex-buffers.md)
</dt> </dl>

 

 
