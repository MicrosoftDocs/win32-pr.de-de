---
title: Einführung in Puffer in Direct3D 11
description: Eine Pufferressource ist eine Sammlung vollständig typisierter Daten, die in Elemente gruppiert sind.
ms.assetid: e33ca01e-f13c-4f91-b0db-2b2bc6b4fd8f
keywords:
- konstanter Puffer, was ist
- Vertexpuffer, was ist
- Indexpuffer, was ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51f7b0dbd60264b77f9d9dc83f39cbb4325464079d537c3ee741a942d26a139
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752020"
---
# <a name="introduction-to-buffers-in-direct3d-11"></a>Einführung in Puffer in Direct3D 11

Eine Pufferressource ist eine Sammlung vollständig typisierter Daten, die in Elemente gruppiert sind. Sie können Puffer verwenden, um eine Vielzahl von Daten zu speichern, einschließlich Positionsvektoren, normaler Vektoren, Texturkoordinaten in einem Scheitelpunktpuffer, Indizes in einem Indexpuffer oder Gerätezustand. Ein Pufferelement besteht aus 1 bis 4 Komponenten. Pufferelemente können gepackte Datenwerte (z. B. R8G8B8A8-Oberflächenwerte), einzelne 8-Bit-Ganzzahlen oder vier 32-Bit-Gleitkommawerte enthalten.

Ein Puffer wird als unstrukturierte Ressource erstellt. Da er unstrukturiert ist, darf ein Puffer keine Mipmapebenen enthalten, er kann beim Lesen nicht gefiltert werden und kann nicht mehrfach sampelt werden.

## <a name="buffer-types"></a>Puffertypen

Die folgenden Pufferressourcentypen werden von Direct3D 11 unterstützt. Alle Puffertypen werden von der [**ID3D11Buffer-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) gekapselt.

-   [Vertexpuffer](#vertex-buffer)
-   [Indexpuffer](#index-buffer)
-   [Konstantenpuffer](#constant-buffer)

### <a name="vertex-buffer"></a>Vertexpuffer

Ein Scheitelpunktpuffer enthält die Scheitelpunktdaten, die zum Definieren der Geometrie verwendet werden. Scheitelpunktdaten umfassen Positionskoordinaten, Farbdaten, Texturkoordinatendaten, normale Daten usw.

Das einfachste Beispiel für einen Scheitelpunktpuffer ist ein Puffer, der nur Positionsdaten enthält. Sie kann wie in der folgenden Abbildung visualisiert werden.

![Abbildung eines Scheitelpunktpuffers, der Positionsdaten enthält](images/d3d10-resources-single-element-vb2.png)

Häufiger enthält ein Scheitelpunktpuffer alle Daten, die zum vollständigen Angeben von 3D-Scheitelpunkten erforderlich sind. Ein Beispiel hierfür ist ein Scheitelpunktpuffer, der die Position pro Scheitelpunkt, normale Koordinaten und Texturkoordinaten enthält. Diese Daten sind in der Regel wie in der folgenden Abbildung dargestellt als Sätze von Pro-Scheitelpunkt-Elementen organisiert.

![Abbildung eines Scheitelpunktpuffers, der Positions-, Normal- und Texturdaten enthält](images/d3d10-vertex-buffer-element.png)

Dieser Scheitelpunktpuffer enthält Daten pro Scheitelpunkt. Jeder Scheitelpunkt speichert drei Elemente (Position, Normal und Texturkoordinaten). Die Position und die Normalität werden in der Regel mit drei 32-Bit-Gleitkomma (DXGI \_ FORMAT \_ R32G32B32 \_ FLOAT) und den Texturkoordinaten mit zwei 32-Bit-Gleitkomma (DXGI \_ FORMAT \_ R32G32 \_ FLOAT) angegeben.

Für den Zugriff auf Daten aus einem Scheitelpunktpuffer müssen Sie wissen, auf welchen Scheitelpunkt zugegriffen werden soll, sowie die folgenden zusätzlichen Pufferparameter:

-   Offset: Die Anzahl der Bytes vom Anfang des Puffers bis zu den Daten für den ersten Scheitelpunkt. Sie können den Offset mithilfe der [**ID3D11DeviceContext::IASetVertexBuffers-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) angeben.
-   BaseVertexLocation: Die Anzahl der Bytes vom Offset bis zum ersten Scheitelpunkt, der vom entsprechenden Draw-Aufruf verwendet wird.

Bevor Sie einen Scheitelpunktpuffer erstellen, müssen Sie dessen Layout definieren, indem Sie eine [**ID3D11InputLayout-Schnittstelle**](/windows/win32/api/d3d11/nn-d3d11-id3d11inputlayout) erstellen. Dies erfolgt durch Aufrufen der [**ID3D11Device::CreateInputLayout-Methode.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout) Nachdem das Eingabelayoutobjekt erstellt wurde, können Sie es an die Eingabeassembliererphase binden, indem Sie [**id3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout)aufrufen.

Um einen Scheitelpunktpuffer zu erstellen, rufen Sie [**ID3D11Device::CreateBuffer auf.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)

### <a name="index-buffer"></a>Indexpuffer

Indexpuffer enthalten ganzzahlige Offsets in Scheitelpunktpuffer und werden verwendet, um Primitive effizienter zu rendern. Ein Indexpuffer enthält einen sequenziellen Satz von 16-Bit- oder 32-Bit-Indizes. jeder Index wird verwendet, um einen Scheitelpunkt in einem Scheitelpunktpuffer zu identifizieren. Ein Indexpuffer kann wie in der folgenden Abbildung visualisiert werden.

![Abbildung eines Indexpuffers](images/d3d10-index-buffer.png)

Die in einem Indexpuffer gespeicherten sequenziellen Indizes befinden sich mit den folgenden Parametern:

-   Offset: Die Anzahl der Bytes aus der Basisadresse des Indexpuffers. Der Offset wird für die [**ID3D11DeviceContext::IASetIndexBuffer-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer) bereitgestellt.
-   StartIndexLocation: Gibt das erste Indexpufferelement aus der Basisadresse und den Offset an, der in [**IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer)bereitgestellt wird. Der Startspeicherort wird für die [**Id3D11DeviceContext::D rawIndexed-**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) oder [**ID3D11DeviceContext::D rawIndexedInstanced-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) angegeben und stellt den ersten zu renderden Index dar.
-   IndexCount: Die Anzahl der zu rendernden Indizes. Die Zahl wird für die [**DrawIndexed-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed) angegeben.

Start des Indexpuffers = Basisadresse des Indexpuffers + Offset (Bytes) + StartIndexLocation \* ElementSize (Bytes);

In dieser Berechnung ist ElementSize die Größe jedes Indexpufferelements, das entweder zwei oder vier Bytes beträgt.

Um einen Indexpuffer zu erstellen, rufen Sie [**ID3D11Device::CreateBuffer auf.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)

### <a name="constant-buffer"></a>Konstantenpuffer

Mit einem Konstantenpuffer können Sie Shaderkonstantendaten effizient für die Pipeline bereitstellen. Sie können einen konstanten Puffer verwenden, um die Ergebnisse der Streamausgabephase zu speichern. Konzeptionell sieht ein konstanter Puffer wie ein Vertexpuffer mit einem einzelnen Element aus, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Shaderkonstantenpuffers](images/d3d10-shader-resource-buffer.png)

Jedes Element speichert eine 1:4-Komponentenkonstante, die durch das Format der gespeicherten Daten bestimmt wird. Um einen Shaderkonstantenpuffer zu erstellen, rufen [**Sie ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) auf, und geben Sie den **D3D11 \_ BIND CONSTANT \_ \_ BUFFER-Member** des [**D3D11 \_ BIND FLAG-Enumerationstyps \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) an.

Ein Konstantenpuffer kann nur ein einzelnes Bindungsflag **(D3D11 \_ BIND \_ CONSTANT \_ BUFFER)** verwenden, das nicht mit einem anderen Bindungsflag kombiniert werden kann. Um einen Shaderkonstantenpuffer an die Pipeline zu binden, rufen Sie eine der folgenden Methoden auf: [**ID3D11DeviceContext::GSSetConstantBuffers,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetconstantbuffers) [**ID3D11DeviceContext::P SSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers)oder [**ID3D11DeviceContext::VSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers).

Um einen Shaderkonstantenpuffer aus einem Shader zu lesen, verwenden Sie eine HLSL-Ladefunktion (z.B. [**Laden).**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load) Jede Shaderstufe lässt bis zu 15 Shaderkonstantenpuffer zu. jeder Puffer kann bis zu 4.096 Konstanten enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Puffer](overviews-direct3d-11-resources-buffers.md)
</dt> </dl>

 

 