---
title: Einführung in Puffer in Direct3D 11
description: Eine Puffer Ressource ist eine Auflistung von vollständig typisierten Daten, die in-Elementen gruppiert sind.
ms.assetid: e33ca01e-f13c-4f91-b0db-2b2bc6b4fd8f
keywords:
- konstanter Puffer, was ist
- Vertex-Puffer, was ist
- Index Puffer, was ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241ade0721ae87b1371586bc901ee18f8975b53f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315452"
---
# <a name="introduction-to-buffers-in-direct3d-11"></a>Einführung in Puffer in Direct3D 11

Eine Puffer Ressource ist eine Auflistung von vollständig typisierten Daten, die in-Elementen gruppiert sind. Sie können Puffer verwenden, um eine Vielzahl von Daten zu speichern, z. b. Positions Vektoren, normale Vektoren, Texturkoordinaten in einem Vertex-Puffer, Indizes in einem Index Puffer oder einen Gerätezustand. Ein Puffer Element besteht aus 1 bis 4 Komponenten. Puffer Elemente können gepackte Datenwerte (z. b. R8G8B8A8 Surface Values), einzelne 8-Bit-Ganzzahlen oder Gleit Komma Werte mit 4 32 Bit enthalten.

Ein Puffer wird als unstrukturierte Ressource erstellt. Da ein Puffer nicht strukturiert ist, kann er keine MipMap-Ebenen enthalten, er kann beim Lesen nicht gefiltert werden und kann nicht mit einem Multisampling verwendet werden.

## <a name="buffer-types"></a>Puffer Typen

Die folgenden Puffer Ressourcentypen werden von Direct3D 11 unterstützt. Alle Puffer Typen werden von der [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) -Schnittstelle gekapselt.

-   [Vertex-Puffer](#vertex-buffer)
-   [Indexpuffer](#index-buffer)
-   [Konstanter Puffer](#constant-buffer)

### <a name="vertex-buffer"></a>Vertex-Puffer

Ein Vertex-Puffer enthält die Vertexdaten, die zum Definieren der Geometrie verwendet werden. Vertex-Daten enthalten Positionskoordinaten, Farbdaten, Texturkoordinaten Daten, normale Daten usw.

Das einfachste Beispiel für einen Vertex-Puffer ist eine, die nur Positionsdaten enthält. Es kann wie in der folgenden Abbildung dargestellt werden.

![Abbildung eines Scheitelpunkt Puffers, der Positionsdaten enthält](images/d3d10-resources-single-element-vb2.png)

Häufig enthält ein Vertex-Puffer alle Daten, die erforderlich sind, um 3D-Vertices vollständig anzugeben. Ein Beispiel hierfür könnte ein Vertex-Puffer sein, der die Position des einzelnen Vertex, die normalen und die Texturkoordinaten enthält. Diese Daten werden in der Regel als Sätze von pro-Vertex-Elementen organisiert, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Scheitelpunkt Puffers, der Positions-, normal-und Textur Daten enthält](images/d3d10-vertex-buffer-element.png)

Dieser Vertex-Puffer enthält pro-Vertex-Daten. jeder Scheitelpunkt speichert drei Elemente (Positions-, normal-und Texturkoordinaten). Die Position und normal werden üblicherweise mit 3 32-Bit-Gleit Komma Zahlen (DXGI- \_ Format \_ R32G32B32 \_ float) und den Texturkoordinaten mit 2 32-Bit-Gleit Komma Zahlen (DXGI- \_ Format \_ R32G32 \_ float) angegeben.

Für den Zugriff auf Daten aus einem Vertex-Puffer müssen Sie wissen, auf welchen Scheitelpunkt zugegriffen werden soll. Außerdem müssen Sie die folgenden zusätzlichen Puffer Parameter angeben:

-   Offset: die Anzahl der Bytes vom Anfang des Puffers bis zu den Daten für den ersten Scheitelpunkt. Sie können den Offset mithilfe der [**Verknüpfung id3d11devicecontext aus:: iasetvertexbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) -Methode angeben.
-   Basevertexlocation: die Anzahl der Bytes vom Offset bis zum ersten Vertex, der vom entsprechenden zeichnen-Befehl verwendet wird.

Vor dem Erstellen eines Scheitelpunkt Puffers müssen Sie sein Layout definieren, indem Sie eine [**ID3D11InputLayout**](/windows/win32/api/d3d11/nn-d3d11-id3d11inputlayout) -Schnittstelle erstellen. Dies erfolgt durch Aufrufen der [**ID3D11Device:: createinputlayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout) -Methode. Nachdem das Eingabe Layout-Objekt erstellt wurde, können Sie es mit der Eingabe-Assembler-Phase durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: iasetinputlayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout)binden.

Rufen Sie zum Erstellen eines Scheitelpunkt Puffers [**ID3D11Device:: up Buffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)auf.

### <a name="index-buffer"></a>Indexpuffer

Index Puffer enthalten ganzzahlige Offsets in Scheitelpunkt Puffer und dienen zum effizienteren Rendering von primitiven. Ein Index Puffer enthält einen sequenziellen Satz von 16-Bit-oder 32-Bit-Indizes. Jeder Index wird zum Identifizieren eines Scheitel Punkts in einem Scheitelpunkt Puffer verwendet. Ein Index Puffer kann wie in der folgenden Abbildung dargestellt werden.

![Abbildung eines Index Puffers](images/d3d10-index-buffer.png)

Die in einem Index Puffer gespeicherten sequenziellen Indizes befinden sich mit den folgenden Parametern:

-   Offset: die Anzahl von Bytes aus der Basisadresse des Index Puffers. Der Offset wird der [**Verknüpfung id3d11devicecontext aus:: iasetindexbuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer) -Methode bereitgestellt.
-   Startindexlocation: gibt das erste Index Puffer Element aus der Basisadresse und den Offset an, der in [**iasetindexbuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer)bereitgestellt wird. Die Startposition wird an die [**Verknüpfung id3d11devicecontext aus::D rawindexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) -oder [**Verknüpfung id3d11devicecontext aus::D rawindexedinstanxed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) -Methode übergeben und stellt den ersten zu Rendering-Index dar.
-   IndexCount: die Anzahl der zu renderenden Indizes. Die Zahl wird der [**drawindexed**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) -Methode bereitgestellt.

Anfang des Index Puffers = Basisadresse des Index Puffers + Offset (Bytes) + startindexlocation \* Element Size (Bytes);

In dieser Berechnung entspricht Element Size der Größe der einzelnen Index Puffer Elemente, die entweder zwei oder vier Bytes groß sind.

Um einen Index Puffer zu erstellen, rufen Sie [**ID3D11Device:: up Buffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)auf.

### <a name="constant-buffer"></a>Konstanter Puffer

Ein konstanter Puffer ermöglicht die effiziente Bereitstellung von Shader-Konstanten Daten an die Pipeline. Sie können einen konstanten Puffer verwenden, um die Ergebnisse der Stream-Output-Phase zu speichern. Konzeptionell sieht ein konstanter Puffer wie in der folgenden Abbildung dargestellt genau wie ein Einzelelement-Vertex-Puffer aus.

![Abbildung eines Shaders-konstantenpuffers](images/d3d10-shader-resource-buffer.png)

Jedes Element speichert eine 1-zu-4-Komponenten Konstante, die durch das Format der gespeicherten Daten bestimmt wird. Um einen Shader-Constant-Puffer zu erstellen, rufen Sie [**ID3D11Device:: up Buffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) auf, und geben Sie den **D3D11 \_ Bind \_ Constant- \_ Puffer** Mitglied des enumerierten Typs [**D3D11 \_ Bind \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) an.

Ein konstanter Puffer kann nur ein einzelnes Bindungsflag (**D3D11 \_ Bind \_ Constant \_ buffer**) verwenden, das nicht mit einem anderen Bindungsflag kombiniert werden kann. Um einen Shader-Konstantenpuffer an die Pipeline zu binden, wenden Sie eine der folgenden Methoden an: [**Verknüpfung id3d11devicecontext aus:: gssetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers), [**Verknüpfung id3d11devicecontext aus::P ssetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers)oder [**Verknüpfung id3d11devicecontext aus:: vssetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers).

Um einen Shader-Konstantenpuffer aus einem Shader zu lesen, verwenden Sie eine HLSL-Ladefunktion (z. b. " [**Laden**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)"). Jede Shader-Stufe ermöglicht bis zu 15 Shader-Konstante Puffer. jeder Puffer kann bis zu 4096 Konstanten enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Puffer](overviews-direct3d-11-resources-buffers.md)
</dt> </dl>

 

 