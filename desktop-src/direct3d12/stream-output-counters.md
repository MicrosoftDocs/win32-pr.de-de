---
title: Streamausgabe-Leistungsindikatoren
description: Die Streamausgabe ist die Fähigkeit der GPU, Scheitelpunkte in einen Puffer zu schreiben. Die Streamausgabeindikatoren überwachen den Fortschritt.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00cc3d78314b5c9130f69c65ebc5fa056d51d7305135025ecf2e4329ecbe6350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989470"
---
# <a name="stream-output-counters"></a>Streamausgabe-Leistungsindikatoren

Die Streamausgabe ist die Fähigkeit der GPU, Scheitelpunkte in einen Puffer zu schreiben. Die Streamausgabeindikatoren überwachen den Fortschritt.

-   [Unterschiede bei Streamzählern von Direct3D 11 zu Direct3D 12](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [BufferFilledSize](#bufferfilledsize)
-   [Zugehörige Themen](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a>Unterschiede bei Streamzählern von Direct3D 11 zu Direct3D 12

Im Rahmen des Streamausgabeprozesses muss die GPU den aktuellen Speicherort im Puffer kennen, in den sie schreibt. In Direct3D 11 wird der Speicher zum Speichern dieses Speicherorts vom Treiber belegt, und anwendungen können diesen Wert nur über die **SOSetTargets-Methode** bearbeiten. In Direct3D 12 belegen Apps Arbeitsspeicher, um diesen aktuellen Speicherort zu speichern. Es gibt keine besonderen Möglichkeiten, diesen Wert zu bearbeiten, und Apps können den Wert mit der CPU oder GPU lesen/schreiben.

## <a name="bufferfilledsize"></a>BufferFilledSize

Die Anwendung ist für die Zuweisung von Speicher für eine 32-Bit-Menge namens *BufferFilledSize* verantwortlich. Dies enthält die Anzahl der Datenbytes im Streamausgabepuffer. Dieser Speicher kann in derselben oder einer anderen Ressource platziert werden wie die Ressource, die die Streamausgabedaten enthält. Auf diesen Wert wird von der GPU in der Streamausgabephase zugegriffen, um zu bestimmen, wo neue Scheitelpunktdaten im Puffer angefügt werden sollen. Darüber hinaus greift die GPU auf diesen Wert zu, um zu ermitteln, wann ein Überlauf aufgetreten ist.

Weitere Informationen finden Sie in der Struktur [**D3D12 \_ STREAM \_ OUTPUT \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).

Die Debugebene überprüft Folgendes in [**ID3D12GraphicsCommandList::SOSetTargets:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)

-   *BufferFilledSize* liegt im Bereich von {*OffsetInBytes*, *SizeInBytes*}, wenn eine Ressource ungleich NULL angegeben wird.
-   *BufferFilledSizeOffsetInBytes* ist ein Vielfaches von 4.
-   *BufferFilledSizeOffsetInBytes* liegt innerhalb des Bereichs der enthaltenden Ressource.
-   Die angegebene Ressource ist ein Puffer.

Die Runtime überprüft nicht den Heaptyp, der dem Streamausgabepuffer zugeordnet ist, da die Streamausgabe in allen Heaptypen unterstützt wird.

Stammsignaturen müssen mithilfe der [**Flags D3D12 \_ ROOT SIGNATURE \_ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) angeben, ob die Streamausgabe verwendet wird.

D3D12 \_ ROOT SIGNATURE FLAG ALLOW STREAM OUTPUT kann für in \_ \_ \_ \_ \_ HLSL erstellte Stammsignaturen auf ähnliche Weise wie die anderen Flags angegeben werden.

[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) schlägt fehl, wenn der geometry-Shader stream-output enthält, aber für die Stammsignatur das Flag D3D12 \_ ROOT SIGNATURE FLAG ALLOW STREAM OUTPUT nicht festgelegt \_ \_ \_ \_ \_ ist.

Wenn eine Ressource als Streamausgabeziel verwendet wird, müssen sich die verwendeten Ressourcen im Zustand D3D12 \_ RESOURCE STATE STREAM OUT \_ \_ \_ befinden. Dies gilt sowohl für die Scheitelpunktdaten als auch für *BufferFilledSize* (die sich in denselben oder separaten Ressourcen enthalten können).

Es gibt keine speziellen APIs zum Festlegen von Pufferoffsets für stream-output, da Anwendungen direkt mit der CPU oder GPU in *BufferFilledSize* schreiben können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Leistungsindikatoren und Abfragen](counters-and-queries.md)
</dt> </dl>

 

 




