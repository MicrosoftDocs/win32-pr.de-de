---
title: Indirektes zeichnen
description: Indirektes zeichnen ermöglicht das Verschieben von Szenen Durchlauf und-Daten aus der CPU auf die GPU, wodurch die Leistung verbessert werden kann. Der Befehls Puffer kann von der CPU oder GPU generiert werden.
ms.assetid: F8D6C88A-101E-4F66-999F-43206F6527B6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7731a662bc6064e635d68942e6b0b222adf1eda8
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/19/2020
ms.locfileid: "104548649"
---
# <a name="indirect-drawing"></a>Indirektes zeichnen

Indirektes zeichnen ermöglicht das Verschieben von Szenen Durchlauf und-Daten aus der CPU auf die GPU, wodurch die Leistung verbessert werden kann. Der Befehls Puffer kann von der CPU oder GPU generiert werden.

-   [Befehls Signaturen](#command-signatures)
-   [Indirekte Argument Puffer Strukturen](#indirect-argument-buffer-structures)
-   [Befehls Signatur Erstellung](#command-signature-creation)
    -   [Keine Argument Änderungen](#no-argument-changes)
    -   [Stamm Konstanten und Vertex-Puffer](#root-constants-and-vertex-buffers)
-   [Verwandte Themen](#related-topics)

## <a name="command-signatures"></a>Befehls Signaturen

Das Befehls Signatur Objekt ([**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature)) ermöglicht es apps, indirekte Zeichnungen anzugeben, insbesondere die folgenden Einstellungen:

-   Das indirekte Argument Puffer Format.
-   Der Befehlstyp, der verwendet wird (aus den [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) -Methoden [**drawinstanused**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced), [**drawindexedinstanused**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)oder [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)).
-   Der Satz von Ressourcen Bindungen, der den pro-Befehl-Rückruf und den Satz ändert, der geerbt wird.

Beim Start erstellt eine APP einen kleinen Satz von **Befehls Signaturen**. Zur Laufzeit füllt die Anwendung einen Puffer mit Befehlen (über das, was der App-Entwickler entscheidet). Die Befehle, die optional den Status für Vertex-Puffer Sichten, Index Puffer Sichten, Stamm Konstanten und Stamm Deskriptoren (RAW oder strukturierte SRV/UAV/cbvs) enthalten. Diese Argument Layouts sind nicht Hardware spezifisch, sodass Apps die Puffer direkt generieren können. Die Befehls Signatur erbt den restlichen Zustand von der Befehlsliste. Dann ruft die APP [**executeindirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) auf, um die GPU anzuweisen, den Inhalt des indirekten Argument Puffers entsprechend dem von einer bestimmten Befehls Signatur definierten Format zu interpretieren.

Wenn die Befehls Signatur root-Argumente ändert, wird diese in der Befehls Signatur als Teilmenge einer Stamm Signatur gespeichert.

Beachten Sie, dass kein Befehls Signatur Zustand an die Befehlsliste zurückgibt, wenn die Ausführung vollständig ist.

Angenommen, ein App-Entwickler möchte, dass eine eindeutige Stamm Konstante im indirekten Argument Puffer pro zeichnen-Befehl angegeben wird. Die APP würde eine Befehls Signatur erstellen, die es dem indirekten Argument Puffer ermöglicht, die folgenden Parameter pro zeichnen-Befehl anzugeben:

-   Der Wert einer Stamm Konstante.
-   Die zeichnen-Argumente (Scheitelpunkt Anzahl, Instanzanzahl usw.).

Der indirekte Argument Puffer, der von der Anwendung generiert wird, enthält ein Array von Datensätzen mit fester Größe. Jede Struktur entspricht einem zeichnen-Befehl. Jede Struktur enthält die Zeichnungs Argumente und den Wert der Stamm Konstante. Die Anzahl der Draw-Aufrufe wird in einem separaten GPU-sichtbaren Puffer angegeben.

Ein Beispiel für einen von der APP generierten Befehls Puffer lautet folgendermaßen:

![Befehls Puffer Format](images/indirect-drawing-command-buffer.png)

## <a name="indirect-argument-buffer-structures"></a>Indirekte Argument Puffer Strukturen

Die folgenden Strukturen definieren, wie bestimmte Argumente in einem indirekten Argument Puffer angezeigt werden. Diese Strukturen werden in keiner D3D12-API angezeigt. Anwendungen verwenden diese Definitionen beim Schreiben in einen indirekten Argument Puffer (mit der CPU oder GPU):

-   [**D3D12 \_ Zeichnen von \_ Argumenten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments)
-   [**D3D12 \_ \_ indizierte \_ Argumente zeichnen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments)
-   [**D3D12 \_ \_ dispatchargumente**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments)
-   [**D3D12 \_ Vertex- \_ Puffer \_ Ansicht**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)
-   [**D3D12 \_ Index \_ Puffer \_ Ansicht**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view)
-   D3D12 \_ GPU \_ Virtual \_ Address (ein TypeDef-Synonym von UINT64).
-   [**D3D12 \_ Konstante \_ Puffer \_ Ansicht**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc)

## <a name="command-signature-creation"></a>Befehls Signatur Erstellung

Verwenden Sie zum Erstellen einer Befehls Signatur die folgenden API-Elemente:

-   [**ID3D12Device:: kreatecommandsignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) (gibt ein [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature)-Ereignis aus)
-   [**D3D12 \_ indirekter \_ \_ Argumenttyp**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type)
-   [**D3D12 \_ indirektes \_ Argument \_ Entsc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc)
-   [**D3D12 \_ Befehls \_ Signatur \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc)

Die Reihenfolge der Argumente innerhalb eines indirekten Argument Puffers wird so definiert, dass Sie genau mit der Reihenfolge der Argumente übereinstimmt, die im *parguments* -Parameter der [**D3D12 \_ Command \_ Signature \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc)angegeben sind. Alle Argumente für einen zeichnen (graphics)/Dispatch (Compute)-Befehl innerhalb eines indirekten Argument Puffers sind eng gepackt. Allerdings dürfen Anwendungen einen beliebigen Byte Schritt zwischen den Draw-/dispatchbefehlen in einem indirekten Argument Puffer angeben.

Die Stamm Signatur muss nur dann angegeben werden, wenn die Befehls Signatur eines der root-Argumente ändert.

Für den Stamm-SRV/UAV/CBV wird die angegebene Größe in Bytes angegeben. Die debugschicht überprüft die folgenden Einschränkungen für die Adresse:

-   CBV – Address muss ein Vielfaches von 256 Bytes sein.
-   Die –-Rohdaten für unformatierte SRV/UAV müssen ein Vielfaches von 4 Bytes sein.
-   Die strukturierte SRV/UAV-–-Adresse muss ein Vielfaches des Struktur Byte Stride (im Shader deklariert) sein.

Eine angegebene Befehls Signatur ist entweder eine zeichnen-oder eine COMPUTE-Befehls Signatur. Wenn eine Befehls Signatur einen Zeichnungs Vorgang enthält, handelt es sich um eine Grafik Befehls Signatur. Andernfalls muss die Befehls Signatur einen dispatchvorgang enthalten, und es handelt sich um eine COMPUTE-Befehls Signatur.

In den folgenden Abschnitten werden einige Beispiel-Befehls Signaturen gezeigt.

### <a name="no-argument-changes"></a>Keine Argument Änderungen

In diesem Beispiel enthält der indirekte Argument Puffer, der von der Anwendung generiert wird, ein Array von 36-Byte-Strukturen. Jede Struktur enthält nur die fünf Parameter, die an [**drawindexedinstan}**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) (plus Padding) übermittelt werden.

Der Code zum Erstellen der Befehls Signatur Beschreibung folgt:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[1];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INDEXED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 36;
ProgramDesc.NumArgumentDescs = 1;
ProgramDesc.pArguments = Args;
```

Das Layout einer einzelnen Struktur innerhalb eines indirekten Argument Puffers lautet:



| Byte | Beschreibung           |
|-------|-----------------------|
| 0:3   | Indexrattperinstance |
| 4:7   | InstanceCount         |
| 8:11  | Startindexlocation    |
| 12:15 | Basevertexlocation    |
| 16:19 | Startinstancelokation |
| 20:35 | Auffüllen               |



 

### <a name="root-constants-and-vertex-buffers"></a>Stamm Konstanten und Vertex-Puffer

In diesem Beispiel ändert jede Struktur in einem indirekten Argument Puffer zwei Stamm Konstanten, ändert eine Vertex-Puffer Bindung und führt einen nicht indizierten Zeichnungs Vorgang aus. Es gibt keine Auffüll Zeichen zwischen Strukturen.

Der Code zum Erstellen der Befehls Signatur Beschreibung lautet:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[4];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[0].Constant.RootParameterIndex = 2;

Args[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[1].Constant.RootParameterIndex = 6;

Args[2].Type = D3D12_INDIRECT_ARGUMENT_TYPE_VERTEX_BUFFER_VIEW;
Args[2].VertexBuffer.VBSlot = 3;

Args[3].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INSTANCED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 40;
ProgramDesc.NumArgumentDescs = 4;
ProgramDesc.pArguments = Args;
```

Das Layout einer einzelnen Struktur innerhalb des indirekten Argument Puffers lautet wie folgt:



| Byte | Beschreibung                     |
|-------|---------------------------------|
| 0:3   | Daten für Stamm Parameter Index 2 |
| 4:7   | Daten für Stamm Parameter Index 6 |
| 8:15  | Virtuelle Adresse von VB (64 Bit)  |
| 16:19 | VB-Größe                         |
| 20:23 | VB-Stride                       |
| 24:27 | Vertexrattperinstance          |
| 28:31 | InstanceCount                   |
| 32:35 | Startvertexlocation             |
| 36:39 | Startinstancelokation           |



 

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Video-Tutorials zu DirectX Advanced Learning: Ausführen indirekter und asynchroner GPU-Berechnungen](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[Indirektes zeichnen und GPU-culult: Code Exemplarische Vorgehensweise](indirect-drawing-and-gpu-culling-.md)
</dt> <dt>

[Darstellung](rendering.md)
</dt> </dl>

 

 