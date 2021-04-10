---
description: In der Scheitelpunkt Pipeline der Fixed-Funktion werden die aktuellen Transformations Matrizen für das Gerät angewendet, wenn die Scheitel Punkte in einem Vertex-Puffer verarbeitet werden.
ms.assetid: a882a5c5-b05e-4659-9040-92d3e2ccd89c
title: Vertex-Verarbeitung fester Funktionen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da30dd0fb6cf6e055d8b1bbb31fdfdb01d9e1e20
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124016"
---
# <a name="fixed-function-vertex-processing-direct3d-9"></a>Vertex-Verarbeitung fester Funktionen (Direct3D 9)

In der Scheitelpunkt Pipeline der Fixed-Funktion werden die aktuellen Transformations Matrizen für das Gerät angewendet, wenn die Scheitel Punkte in einem Vertex-Puffer verarbeitet werden. Vertex-Vorgänge, wie z. b. Beleuchtung, das Erzeugen von Clip-Flags und das Aktualisieren von Blöcken, können optional auch angewendet werden. Wenn Sie die Vertex-Verarbeitung fester Funktionen verwenden, wird das Ändern der Elemente im Ziel Vertex-Puffer durch das Flag [D3DPV \_ donotcopydata](other-direct3d-constants.md) gesteuert. Dieses Flag gilt nur für die Verarbeitung fester Funktions Vertex. Die [**IDirect3DDevice9**](/windows/desktop/api) -Schnittstelle macht die [**IDirect3DDevice9::P rocess Vertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) -Methode zum Verarbeiten von Vertices verfügbar. Sie verarbeiten Vertices von einem Vertex-Shader in den Satz von Eingabedaten strömen und erzeugen durch Aufrufen der **IDirect3DDevice9::P rocess Vertices** -Methode einen einzelnen Datenstrom mit verschachtelten Vertex-Daten an den Ziel-Vertex-Puffer. Die-Methode akzeptiert fünf Parameter, die den Speicherort und die Anzahl der Scheitel Punkte der Methode, den Ziel Vertex-Puffer und die Verarbeitungsoptionen beschreiben. Nach dem-Befehl enthält der Ziel Puffer die verarbeiteten Vertex-Daten.

Der erste, zweite und dritte Parameter, srcstartindex, destIndex und VertexCount, geben den Index des ersten zu ladenden Vertex, den Index im Ziel Puffer, an dem die Scheitel Punkte platziert werden, und die Gesamtzahl der zu verarbeitenden Scheitel Punkte im Ziel Puffer an. Der vierte Parameter, pdestbuffer, sollte auf die Adresse der [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) -Schnittstelle des Vertex-Puffer Objekts festgelegt werden, das die Quell Vertices empfängt. Der srcstartindex-Parameter gibt den Index an, an dem die Methode mit der Verarbeitung von Vertices beginnen soll.

Der letzte Parameter, Flags, bestimmt spezielle Verarbeitungsoptionen für die Methode. Sie können diesen Parameter für die Standard Vertex-Verarbeitung auf 0 festlegen, oder auf [D3DPV \_ donotcopydata](other-direct3d-constants.md) , um die Verarbeitung in einigen Situationen zu optimieren. Sie können den D3DPV \_ donotcopydata-Wert auch mit einem oder mehreren [D3DLOCK](d3dlock.md) -Werten kombinieren, die für den Ziel Puffer geeignet sind. Wenn Sie Flags auf 0 festlegen, werden Vertex-Komponenten des Scheitelpunkt Formats des Ziel Vertex-Puffers, die nicht vom Scheitelpunkt Vorgang betroffen sind, weiterhin aus dem Vertexshader kopiert oder auf 0 festgelegt. Wenn jedoch D3DPV \_ donotcopydata verwendet wird, überschreibt [**IDirect3DDevice9::P rocess Vertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) keine Farb-und Texturkoordinaten Informationen im Ziel Puffer, es sei denn, diese Daten werden von Direct3D generiert. Die diffuse Farbe wird generiert, wenn Beleuchtung aktiviert ist, d \_ . h. D3DRS Beleuchtung ist auf **true** festgelegt. Glanz Farbe wird generiert, wenn Beleuchtung aktiviert und Glanz aktiviert ist, \_ d. h. D3DRS specularenable und D3DRS- \_ Beleuchtung auf **true** festgelegt ist. Glanz Farbe wird auch generiert, wenn der Nebel aktiviert ist. Texturkoordinaten werden generiert, wenn Textur Transformation oder Textur Generierung aktiviert ist. **IDirect3DDevice9::P rocess Vertices** verwendet die aktuellen Rendering-Zustände, um zu bestimmen, welche Vertex-Verarbeitung durchgeführt werden soll.

## <a name="fvf-usage-settings-for-destination-vertex-buffers"></a>Bbbjekt-Verwendungs Einstellungen für Ziel Vertex-Puffer

Die [**IDirect3DDevice9::P rocess Vertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) -Methode erfordert bestimmte Einstellungen für den [D3DFVF](d3dfvf.md) des Ziel-Vertex-Puffers. Die Verwendungs Einstellungen von "f VF" müssen mit den aktuellen Einstellungen für die Vertexverarbeitung kompatibel sein.

Für die Vertex-Verarbeitung fester Funktionen erfordert [**IDirect3DDevice9::P rocess Vertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) die folgenden Einstellungen für die "f"-Funktion:

-   Der Positionstyp ist immer [D3DFVF \_ xyzrhw](d3dfvf.md) \_ . Daher sind D3DFVF XYZ und D3DFVF \_ XYZB1 bis D3DFVF \_ XYZB5 ungültig.
-   Die [D3DFVF \_ Normal](d3dfvf.md), D3DFVF \_ RESERVED0 und D3DFVF \_ "reserved2" Flags dürfen nicht festgelegt werden.
-   Das Flag [D3DFVF \_ diffuse](d3dfvf.md) muss festgelegt werden, wenn eine OR-Operation der folgenden Bedingungen true zurückgibt:
    -   Beleuchtung ist aktiviert; Das heißt, D3DRS \_ Beleuchtung ist " **true**".
    -   Beleuchtung ist deaktiviert, diffuse Farbe ist in den eingegebenen Scheitelpunkt Strömen enthalten, und [D3DPV \_ donotcopydata](other-direct3d-constants.md) ist nicht festgelegt.
-   Das Flag [D3DFVF \_ specarität](d3dfvf.md) muss festgelegt werden, wenn eine OR-Operation der folgenden Bedingungen true zurückgibt:
    -   Beleuchtung ist aktiviert, und die Glanz Farbe ist aktiviert. Das heißt, D3DRS \_ specularenable ist " **true**".
    -   Beleuchtung ist deaktiviert, Glanz Farbe ist in den eingegebenen Scheitel Punkten enthalten, und [D3DPV \_ donotcopydata](other-direct3d-constants.md) ist nicht festgelegt.
    -   Scheitelpunkt Nebel ist aktiviert; Das heißt, D3DRS \_ fogvertexmode ist nicht auf D3DFOG None festgelegt \_ .

Außerdem muss die Anzahl der Texturkoordinaten wie folgt festgelegt werden:

-   Wenn Textur Transformation und Textur Generierung für alle aktiven Textur Phasen deaktiviert sind und [D3DPV \_ donotcopydata](other-direct3d-constants.md) nicht festgelegt ist, werden die Anzahl und der Typ der Ausgabe Texturkoordinaten benötigt, damit Sie mit denen der eingegebenen Scheitelpunkt Texturkoordinaten identisch sind. Wenn D3DPV \_ donotcopydata festgelegt ist und Textur Transformation und Textur Generierung deaktiviert sind, werden die Ausgabe Texturkoordinaten ignoriert.
-   Wenn Textur Transformation oder Textur Generierung für alle aktiven Textur Stufen aktiviert ist, muss der Ausgabe Scheitelpunkt möglicherweise mehr Texturkoordinaten Sätze als der Eingabe Scheitelpunkt enthalten. Dies liegt an der Verbreitung von Texturkoordinaten von denjenigen, die von der Textur Generierung generiert oder durch Textur Transformationen abgeleitet werden. Beachten Sie, dass eine ähnliche Verbreitung von Texturkoordinaten während [**IDirect3DDevice9 auftritt::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -Aufrufe, aber für den Anwendungsprogrammierer nicht sichtbar. In diesem Fall generiert Direct3D einen neuen Satz von Texturkoordinaten. Der neue Satz von Texturkoordinaten wird durch schrittweise durchlaufen der Textur Stufen und Analysieren der Einstellungen für die Textur Generierung, Textur Transformation und Texturkoordinaten Index abgeleitet, um zu bestimmen, ob für diese Phase ein eindeutiger Satz von Texturkoordinaten erforderlich ist. Jedes Mal, wenn ein neuer Satz erforderlich ist, wird er in steigender Reihenfolge zugeordnet. Beachten Sie, dass die maximale und typische Anforderung eine Menge pro Phase ist, obwohl Sie möglicherweise aufgrund der Freigabe von nicht transformierten Texturkoordinaten über D3DTSS \_ texcoordindex weniger stark ist.

Daher wird für jede Textur Phase ein neuer Satz von Texturkoordinaten generiert, wenn eine Textur an diese Phase gebunden ist und eine der folgenden Bedingungen zutrifft:

-   Die Textur Generierung ist für diese Phase aktiviert.
-   Die Textur Transformation ist für diese Phase aktiviert.
-   Auf nicht transformierte Eingabe Texturkoordinaten wird über D3DTSS \_ texcoordindex zum ersten Mal verwiesen.

Wenn Direct3D Texturkoordinaten erzeugt, muss die Anwendung die folgenden Aktionen ausführen:

1.  Verwenden Sie einen Ziel-Vertex-Puffer mit der entsprechenden Verwendung von "f".
2.  Programmieren Sie den D3DTSS \_ texcoordindex der Textur Phase entsprechend der Platzierung der postverarbeiteten Texturkoordinaten neu. Beachten Sie, dass die Neuprogrammierung der D3DTSS \_ texcoordindex-Einstellung erfolgt, wenn der verarbeitete Vertex-Puffer in nachfolgenden [**IDirect3DDevice9::D rawprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) -und [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) -Aufrufen verwendet wird.

Zum Schluss muss die Dimensionalität der Textur Koordinate ([D3DFVF \_ TEX0](d3dfvf.md) through D3DFVF \_ TEX8) wie folgt festgelegt werden:

-   Wenn die Textur Transformation und die Textur Generierung für jeden Texturkoordinaten Satz deaktiviert sind, muss die Dimensionalität der Ausgabe Textur Koordinate mit der Eingabe identisch sein. Wenn die Textur Transformation aktiviert ist, muss die Ausgabe Dimensionalität der Anzahl entsprechen, die durch die \_ Einstellungen D3DTTFF COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3 oder D3DTTFF \_ COUNT4 definiert wird. Wenn die Textur Transformation deaktiviert ist und die Textur Generierung aktiviert ist, muss die Ausgabe Dimensionalität den Einstellungen für den Textur Generierungs Modus entsprechen. zurzeit generieren alle Modi drei float-Werte.

Wenn [**IDirect3DDevice9::P rocess Vertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) aufgrund eines inkompatiblen Ziel-Vertexpuffers FVF-Codes fehlschlägt, wird der erwartete Code in der Debugausgabe ausgegeben (nur Debugbuilds).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Puffer](vertex-buffers.md)
</dt> </dl>

 

 
