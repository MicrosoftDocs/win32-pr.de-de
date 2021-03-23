---
title: Stream-ausgabezähler
description: Die Streamausgabe ist die Fähigkeit der GPU, Vertices in einen Puffer zu schreiben. Der Status der Datenstrom-ausgabezähler Monitor.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d2f3a823f5f4b5d2d5f365235d7e3f8817207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103570"
---
# <a name="stream-output-counters"></a>Stream-ausgabezähler

Die Streamausgabe ist die Fähigkeit der GPU, Vertices in einen Puffer zu schreiben. Der Status der Datenstrom-ausgabezähler Monitor.

-   [Unterschiede in den Datenstrom Indikatoren von Direct3D 11 bis Direct3D 12](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [Bufferfilledsize](#bufferfilledsize)
-   [Verwandte Themen](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a>Unterschiede in den Datenstrom Indikatoren von Direct3D 11 bis Direct3D 12

Im Rahmen des Datenstrom Ausgabeprozesses muss die GPU die aktuelle Position im Puffer kennen, in die Sie schreibt. In Direct3D 11 wird der Speicherplatz zum Speichern dieses Speicher Orts vom Treiber zugeordnet. die einzige Möglichkeit für Anwendungen, diesen Wert zu bearbeiten, ist die **sosettargets** -Methode. In Direct3D 12 weisen apps Arbeitsspeicher zu, um diesen aktuellen Speicherort zu speichern. Es gibt keine besonderen Möglichkeiten, diesen Wert zu bearbeiten, und Apps können den Wert mit der CPU oder GPU lesen/schreiben.

## <a name="bufferfilledsize"></a>Bufferfilledsize

Die Anwendung ist für die Zuordnung von Speicher für eine 32-Bit-Menge zuständig, die als *bufferfilledsize* bezeichnet wird. Enthält die Anzahl der Daten Bytes im Stream-Ausgabepuffer. Dieser Speicher kann in derselben oder einer anderen Ressource wie die, die die Datenstrom Ausgabedaten enthält, platziert werden. Der Zugriff auf diesen Wert erfolgt durch die GPU in der Stream-Output-Phase, um zu bestimmen, wo neue Scheitelpunkt Daten im Puffer angefügt werden sollen. Außerdem wird auf diesen Wert durch die GPU zugegriffen, um zu bestimmen, wann ein Überlauf aufgetreten ist.

Weitere Informationen finden Sie in der Struktur [**D3D12 \_ Stream \_ Output \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).

Die debugschicht überprüft Folgendes in [**ID3D12GraphicsCommandList:: sosettargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):

-   *Bufferfilledsize* fällt in den Bereich, der von {*offmentinbytes*, *sizeInBytes*} impliziert wird, wenn eine Ressource ungleich NULL angegeben wird.
-   *Bufferfilledsizeofftertinbytes* ist ein Vielfaches von 4.
-   *Bufferfilledsizeoffmentinbytes* liegt innerhalb des Bereichs der enthaltenden Ressource.
-   Die angegebene Ressource ist ein Puffer.

Die Laufzeit überprüft den heaptyp, der dem Datenstrom-Ausgabepuffer zugeordnet ist, nicht, da die Streamausgabe in allen Heap Typen unterstützt wird.

Stamm Signaturen müssen angeben, ob die Datenstrom Ausgabe verwendet werden soll, indem Sie die Flags der [**D3D12 \_ root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) verwenden.

D3D12 \_ root \_ Signature \_ Flag \_ Allow \_ Stream \_ Output kann für Stamm Signaturen angegeben werden, die in HLSL erstellt wurden. Dies ähnelt der Art und Weise, wie die anderen Flags angegeben werden.

Bei " [**kreategraphicspipelinestate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) " tritt ein Fehler auf, wenn der Geometrie-Shader "Stream-Output" enthält, aber die Stamm Signatur nicht das Flag "D3D12 \_ root \_ Signature \_ Flag \_ Allow \_ Stream \_ Output" festgelegt hat.

Wenn eine Ressource als Stream-Ausgabeziel verwendet wird, müssen die verwendeten Ressourcen den \_ \_ \_ Status Stream out für D3D12 Resource State aufweisen \_ . Dies gilt sowohl für Scheitelpunkt Daten als auch für *bufferfilledsize* (die sich in der gleichen oder in separaten Ressourcen befinden können).

Es gibt keine speziellen APIs zum Festlegen von streamausgabepufferoffsets, da Anwendungen direkt mit der CPU oder GPU in *bufferfilledsize* schreiben können.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Zähler und Abfragen](counters-and-queries.md)
</dt> </dl>

 

 




