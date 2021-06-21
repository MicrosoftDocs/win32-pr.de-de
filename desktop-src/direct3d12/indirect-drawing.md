---
title: Indirektes Zeichnen
description: Indirektes Zeichnen ermöglicht es, einige Szenendurchlauf- und Cullingvorgänge von der CPU zur GPU zu verschieben, was die Leistung verbessern kann. Der Befehlspuffer kann von der CPU oder GPU generiert werden.
ms.assetid: F8D6C88A-101E-4F66-999F-43206F6527B6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa474a469d5789d4b31830400d981ea771db2e8
ms.sourcegitcommit: b9a7a48e52219bf8d33e6b8171fc9f8b52151e92
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/21/2021
ms.locfileid: "112421878"
---
# <a name="indirect-drawing"></a>Indirektes Zeichnen

Indirektes Zeichnen ermöglicht es, einige Szenendurchlauf- und Cullingvorgänge von der CPU zur GPU zu verschieben, was die Leistung verbessern kann. Der Befehlspuffer kann von der CPU oder GPU generiert werden.

-   [Befehlssignaturen](#command-signatures)
-   [Indirekte Argumentpufferstrukturen](#indirect-argument-buffer-structures)
-   [Erstellung der Befehlssignatur](#command-signature-creation)
    -   [Keine Argumentänderungen](#no-argument-changes)
    -   [Stammkonstanten und Scheitelpunktpuffer](#root-constants-and-vertex-buffers)
-   [Verwandte Themen](#related-topics)

## <a name="command-signatures"></a>Befehlssignaturen

Mit dem Befehlssignaturobjekt ([**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature)) können Apps indirekte Zeichnungen angeben, insbesondere folgende Einstellungen:

-   Das Pufferformat für indirekte Argumente.
-   Der Befehlstyp, der verwendet wird (von den [**ID3D12GraphicsCommandList-Methoden**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) [**DrawInstanced,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)oder [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)).
-   Der Satz von Ressourcenbindungen, der sich pro Befehlsaufruf im Vergleich zu dem Satz ändert, der geerbt wird.

Beim Start erstellt eine App einen kleinen Satz von **Befehlssignaturen.** Zur Laufzeit füllt die Anwendung einen Puffer mit Befehlen aus (unabhängig davon, was der App-Entwickler wählt). Die Befehle enthalten optional den Zustand, der für Scheitelpunktpuffersichten, Indexpuffersichten, Stammkonstanten und Stammdeskriptoren (unformatierte oder strukturierte SRV-/UAV-/CBVs) festgelegt werden soll. Diese Argumentlayouts sind nicht hardwarespezifisch, sodass Apps die Puffer direkt generieren können. Die Befehlssignatur erbt den verbleibenden Zustand aus der Befehlsliste. Anschließend ruft die App [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) auf, um die GPU anzuweisen, den Inhalt des indirekten Argumentpuffers gemäß dem Format zu interpretieren, das von einer bestimmten Befehlssignatur definiert wird.

Wenn die Befehlssignatur Stammargumente ändert, wird diese in der Befehlssignatur als Teilmenge einer Stammsignatur gespeichert.

Beachten Sie, dass kein Befehlssignaturzustand in die Befehlsliste zurückfällt, wenn die Ausführung abgeschlossen ist.

Angenommen, ein App-Entwickler möchte eine eindeutige Stammkonstante pro Draw-Aufruf im indirekten Argumentpuffer angeben. Die App erstellt eine Befehlssignatur, die es dem indirekten Argumentpuffer ermöglicht, die folgenden Parameter pro Draw-Aufruf anzugeben:

-   Der Wert einer Stammkonstante.
-   Die Draw-Argumente (Scheitelpunktanzahl, Instanzanzahl usw.).

Der von der Anwendung generierte indirekte Argumentpuffer würde ein Array von Datensätzen fester Größe enthalten. Jede Struktur entspricht einem Zeichnen-Aufruf. Jede -Struktur enthält die Zeichnungsargumente und den Wert der Stammkonstante. Die Anzahl der Zeichnen-Aufrufe wird in einem separaten GPU-sichtbaren Puffer angegeben.

Ein Beispielbefehlspuffer, der von der App generiert wird, lautet wie folgt:

![Befehlspufferformat](images/indirect-drawing-command-buffer.png)

## <a name="indirect-argument-buffer-structures"></a>Indirekte Argumentpufferstrukturen

Die folgenden Strukturen definieren, wie bestimmte Argumente in einem indirekten Argumentpuffer angezeigt werden. Diese Strukturen werden in keiner D3D12-API angezeigt. Anwendungen verwenden diese Definitionen beim Schreiben in einen indirekten Argumentpuffer (mit CPU oder GPU):

-   [**D3D12 \_ \_ DRAW-ARGUMENTE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments)
-   [**D3D12 \_ ZEICHNEN \_ INDIZIERTE \_ ARGUMENTE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments)
-   [**D3D12 \_ \_ DISPATCH-ARGUMENTE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments)
-   [**D3D12 \_ \_ \_ VERTEXPUFFERANSICHT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)
-   [**D3D12 \_ INDEX \_ BUFFER \_ VIEW**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view)
-   D3D12 \_ GPU VIRTUAL ADDRESS \_ \_ (ein typedef'd-Synonym von UINT64).
-   [**D3D12-KONSTANTE \_ \_ \_ PUFFERANSICHT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc)

## <a name="command-signature-creation"></a>Erstellung der Befehlssignatur

Verwenden Sie zum Erstellen einer Befehlssignatur die folgenden API-Elemente:

-   [**ID3D12Device::CreateCommandSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) (gibt eine [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature)aus)
-   [**TYP DES \_ INDIREKTEN D3D12-ARGUMENTS \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type)
-   [**D3D12 \_ INDIRECT \_ ARGUMENT \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc)
-   [**\_ \_ D3D12-BEFEHLSSIGNATUR-DESC \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc)

Die Reihenfolge der Argumente innerhalb eines indirekten Argumentpuffers wird so definiert, dass sie genau der Reihenfolge der Argumente entspricht, die im *pArguments-Parameter* von [**D3D12 \_ COMMAND SIGNATURE \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc)angegeben sind. Alle Argumente für einen Zeichnen-/Verteilungsaufruf (Compute) innerhalb eines indirekten Argumentpuffers sind eng gepackt. Anwendungen dürfen jedoch einen beliebigen Byteschritt zwischen draw/dispatch-Befehlen in einem indirekten Argumentpuffer angeben.

Die Stammsignatur muss nur angegeben werden, wenn die Befehlssignatur eines der Stammargumente ändert.

Für die Stamm-SRV/UAV/CBV beträgt die angegebene Größe der Anwendung in Bytes. Die Debugebene überprüft die folgenden Einschränkungen für die Adresse:

-   CBV: Die Adresse muss ein Vielfaches von 256 Bytes sein.
-   Unformatierte SRV-/UAV-Adresse: Die Adresse muss ein Vielfaches von 4 Bytes sein.
-   Strukturierter SRV/UAV: Die Adresse muss ein Vielfaches des Struktur-Byteschritts sein (im Shader deklariert).

Eine angegebene Befehlssignatur ist entweder eine Draw- oder eine Computebefehlssignatur. Wenn eine Befehlssignatur einen Zeichnungsvorgang enthält, handelt es sich um eine Grafikbefehlssignatur. Andernfalls muss die Befehlssignatur einen Dispatchvorgang enthalten, und es handelt sich um eine Computebefehlssignatur.

In den folgenden Abschnitten werden einige Beispielbefehlssignaturen gezeigt.

### <a name="no-argument-changes"></a>Keine Argumentänderungen

In diesem Beispiel enthält der von der Anwendung generierte indirekte Argumentpuffer ein Array von 36-Byte-Strukturen. Jede Struktur enthält nur die fünf Parameter, die an [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) (plus Auffüllung) übergeben werden.

Der Code zum Erstellen der Befehlssignaturbeschreibung lautet wie folgt:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[1];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INDEXED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 36;
ProgramDesc.NumArgumentDescs = 1;
ProgramDesc.pArguments = Args;
```

Das Layout einer einzelnen Struktur innerhalb eines indirekten Argumentpuffers lautet:



| Byte | Beschreibung           |
|-------|-----------------------|
| 0:3   | IndexCountPerInstance |
| 4:7   | InstanceCount         |
| 8:11  | StartIndexLocation    |
| 12:15 | BaseVertexLocation    |
| 16:19 | StartInstanceLocation |
| 20:35 | Auffüllen               |



 

### <a name="root-constants-and-vertex-buffers"></a>Stammkonstanten und Scheitelpunktpuffer

In diesem Beispiel ändert jede Struktur in einem indirekten Argumentpuffer zwei Stammkonstanten, ändert eine Vertexpufferbindung und führt einen nicht indizierten Zeichnungsvorgang aus. Es gibt keine Auffüllung zwischen Strukturen.

Der Code zum Erstellen der Befehlssignaturbeschreibung lautet:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[4];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[0].Constant.RootParameterIndex = 2;
Args[0].Constant.DestOffsetIn32BitValues = 0;
Args[0].Constant.Num32BitValuesToSet = 1;

Args[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[1].Constant.RootParameterIndex = 6;
Args[1].Constant.DestOffsetIn32BitValues = 0;
Args[1].Constant.Num32BitValuesToSet = 1;

Args[2].Type = D3D12_INDIRECT_ARGUMENT_TYPE_VERTEX_BUFFER_VIEW;
Args[2].VertexBuffer.Slot = 3;

Args[3].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 40;
ProgramDesc.NumArgumentDescs = 4;
ProgramDesc.pArguments = Args;
```

Das Layout einer einzelnen Struktur innerhalb des indirekten Argumentpuffers sieht wie folgt aus:



| Byte | Beschreibung                               |
|-------|-------------------------------------------|
| 0:3   | Daten für den Stammparameterindex 2           |
| 4:7   | Daten für den Stammparameterindex 6           |
| 8:15  | Virtuelle Adresse von VB im Slot 3 (64-Bit)  |
| 16:19 | VB-Größe                                   |
| 20:23 | VB-Stride                                 |
| 24:27 | VertexCountPerInstance                    |
| 28:31 | InstanceCount                             |
| 32:35 | StartVertexLocation                       |
| 36:39 | StartInstanceLocation                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videotutorials für erweitertes Lernen mit DirectX: Ausführen der indirekten und asynchronen GPU-Culling](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[Indirektes Zeichnen und GPU-Culling: exemplarische Vorgehensweise für Code](indirect-drawing-and-gpu-culling-.md)
</dt> <dt>

[Darstellung](rendering.md)
</dt> </dl>

 

 
