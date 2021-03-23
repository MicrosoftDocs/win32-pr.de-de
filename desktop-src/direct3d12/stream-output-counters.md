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
# <a name="stream-output-counters"></a><span data-ttu-id="ea24d-104">Stream-ausgabezähler</span><span class="sxs-lookup"><span data-stu-id="ea24d-104">Stream Output Counters</span></span>

<span data-ttu-id="ea24d-105">Die Streamausgabe ist die Fähigkeit der GPU, Vertices in einen Puffer zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="ea24d-105">Stream output is the ability of the GPU to write vertices to a buffer.</span></span> <span data-ttu-id="ea24d-106">Der Status der Datenstrom-ausgabezähler Monitor.</span><span class="sxs-lookup"><span data-stu-id="ea24d-106">The stream output counters monitor progress.</span></span>

-   [<span data-ttu-id="ea24d-107">Unterschiede in den Datenstrom Indikatoren von Direct3D 11 bis Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ea24d-107">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [<span data-ttu-id="ea24d-108">Bufferfilledsize</span><span class="sxs-lookup"><span data-stu-id="ea24d-108">BufferFilledSize</span></span>](#bufferfilledsize)
-   [<span data-ttu-id="ea24d-109">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ea24d-109">Related topics</span></span>](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="ea24d-110">Unterschiede in den Datenstrom Indikatoren von Direct3D 11 bis Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="ea24d-110">Differences in Stream Counters from Direct3D 11 to Direct3D 12</span></span>

<span data-ttu-id="ea24d-111">Im Rahmen des Datenstrom Ausgabeprozesses muss die GPU die aktuelle Position im Puffer kennen, in die Sie schreibt.</span><span class="sxs-lookup"><span data-stu-id="ea24d-111">As a part of the stream output process, the GPU has to know the current location in the buffer that it is writing to.</span></span> <span data-ttu-id="ea24d-112">In Direct3D 11 wird der Speicherplatz zum Speichern dieses Speicher Orts vom Treiber zugeordnet. die einzige Möglichkeit für Anwendungen, diesen Wert zu bearbeiten, ist die **sosettargets** -Methode.</span><span class="sxs-lookup"><span data-stu-id="ea24d-112">In Direct3D 11, memory to store this location is allocated by the driver and the only way for applications to manipulate this value is via the **SOSetTargets** method.</span></span> <span data-ttu-id="ea24d-113">In Direct3D 12 weisen apps Arbeitsspeicher zu, um diesen aktuellen Speicherort zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ea24d-113">In Direct3D 12, apps allocate memory to store this current location.</span></span> <span data-ttu-id="ea24d-114">Es gibt keine besonderen Möglichkeiten, diesen Wert zu bearbeiten, und Apps können den Wert mit der CPU oder GPU lesen/schreiben.</span><span class="sxs-lookup"><span data-stu-id="ea24d-114">There are no special ways to manipulate this value, and apps are free to read/write the value with the CPU or GPU.</span></span>

## <a name="bufferfilledsize"></a><span data-ttu-id="ea24d-115">Bufferfilledsize</span><span class="sxs-lookup"><span data-stu-id="ea24d-115">BufferFilledSize</span></span>

<span data-ttu-id="ea24d-116">Die Anwendung ist für die Zuordnung von Speicher für eine 32-Bit-Menge zuständig, die als *bufferfilledsize* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="ea24d-116">The application is responsible for allocating storage for a 32-bit quantity called the *BufferFilledSize*.</span></span> <span data-ttu-id="ea24d-117">Enthält die Anzahl der Daten Bytes im Stream-Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="ea24d-117">This contains the number of bytes of data in the stream-output buffer.</span></span> <span data-ttu-id="ea24d-118">Dieser Speicher kann in derselben oder einer anderen Ressource wie die, die die Datenstrom Ausgabedaten enthält, platziert werden.</span><span class="sxs-lookup"><span data-stu-id="ea24d-118">This storage can be placed in the same, or a different, resource as the one that contains the stream-output data.</span></span> <span data-ttu-id="ea24d-119">Der Zugriff auf diesen Wert erfolgt durch die GPU in der Stream-Output-Phase, um zu bestimmen, wo neue Scheitelpunkt Daten im Puffer angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ea24d-119">This value is accessed by the GPU in the stream-output stage to determine where to append new vertex data in the buffer.</span></span> <span data-ttu-id="ea24d-120">Außerdem wird auf diesen Wert durch die GPU zugegriffen, um zu bestimmen, wann ein Überlauf aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ea24d-120">Additionally, this value is accessed by the GPU to determine when overflow has occurred.</span></span>

<span data-ttu-id="ea24d-121">Weitere Informationen finden Sie in der Struktur [**D3D12 \_ Stream \_ Output \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span><span class="sxs-lookup"><span data-stu-id="ea24d-121">Refer to the structure [**D3D12\_STREAM\_OUTPUT\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).</span></span>

<span data-ttu-id="ea24d-122">Die debugschicht überprüft Folgendes in [**ID3D12GraphicsCommandList:: sosettargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span><span class="sxs-lookup"><span data-stu-id="ea24d-122">The debug layer will validate the following in [**ID3D12GraphicsCommandList::SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):</span></span>

-   <span data-ttu-id="ea24d-123">*Bufferfilledsize* fällt in den Bereich, der von {*offmentinbytes*, *sizeInBytes*} impliziert wird, wenn eine Ressource ungleich NULL angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ea24d-123">*BufferFilledSize* falls in the range implied by {*OffsetInBytes*, *SizeInBytes*}, if a non-NULL resource is specified.</span></span>
-   <span data-ttu-id="ea24d-124">*Bufferfilledsizeofftertinbytes* ist ein Vielfaches von 4.</span><span class="sxs-lookup"><span data-stu-id="ea24d-124">*BufferFilledSizeOffsetInBytes* is a multiple of 4.</span></span>
-   <span data-ttu-id="ea24d-125">*Bufferfilledsizeoffmentinbytes* liegt innerhalb des Bereichs der enthaltenden Ressource.</span><span class="sxs-lookup"><span data-stu-id="ea24d-125">*BufferFilledSizeOffsetInBytes* is within the range of the containing resource.</span></span>
-   <span data-ttu-id="ea24d-126">Die angegebene Ressource ist ein Puffer.</span><span class="sxs-lookup"><span data-stu-id="ea24d-126">The specified resource is a buffer.</span></span>

<span data-ttu-id="ea24d-127">Die Laufzeit überprüft den heaptyp, der dem Datenstrom-Ausgabepuffer zugeordnet ist, nicht, da die Streamausgabe in allen Heap Typen unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="ea24d-127">The runtime will not validate the heap type associated with the stream output buffer, as stream output is supported in all heap types.</span></span>

<span data-ttu-id="ea24d-128">Stamm Signaturen müssen angeben, ob die Datenstrom Ausgabe verwendet werden soll, indem Sie die Flags der [**D3D12 \_ root \_ Signature \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) verwenden.</span><span class="sxs-lookup"><span data-stu-id="ea24d-128">Root signatures must specify if stream output will be used, by using the [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags.</span></span>

<span data-ttu-id="ea24d-129">D3D12 \_ root \_ Signature \_ Flag \_ Allow \_ Stream \_ Output kann für Stamm Signaturen angegeben werden, die in HLSL erstellt wurden. Dies ähnelt der Art und Weise, wie die anderen Flags angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ea24d-129">D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT can be specified for root signatures authored in HLSL, in a manner similar to how the other flags are specified.</span></span>

<span data-ttu-id="ea24d-130">Bei " [**kreategraphicspipelinestate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) " tritt ein Fehler auf, wenn der Geometrie-Shader "Stream-Output" enthält, aber die Stamm Signatur nicht das Flag "D3D12 \_ root \_ Signature \_ Flag \_ Allow \_ Stream \_ Output" festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="ea24d-130">[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) will fail if the geometry shader contains stream-output but the root signature does not have the D3D12\_ROOT\_SIGNATURE\_FLAG\_ALLOW\_STREAM\_OUTPUT flag set.</span></span>

<span data-ttu-id="ea24d-131">Wenn eine Ressource als Stream-Ausgabeziel verwendet wird, müssen die verwendeten Ressourcen den \_ \_ \_ Status Stream out für D3D12 Resource State aufweisen \_ .</span><span class="sxs-lookup"><span data-stu-id="ea24d-131">When a resource is used as a stream-output target, the resources used must be in the D3D12\_RESOURCE\_STATE\_STREAM\_OUT state.</span></span> <span data-ttu-id="ea24d-132">Dies gilt sowohl für Scheitelpunkt Daten als auch für *bufferfilledsize* (die sich in der gleichen oder in separaten Ressourcen befinden können).</span><span class="sxs-lookup"><span data-stu-id="ea24d-132">This applies to both the vertex data and the *BufferFilledSize* (which can be in the same or separate resources).</span></span>

<span data-ttu-id="ea24d-133">Es gibt keine speziellen APIs zum Festlegen von streamausgabepufferoffsets, da Anwendungen direkt mit der CPU oder GPU in *bufferfilledsize* schreiben können.</span><span class="sxs-lookup"><span data-stu-id="ea24d-133">There are no special APIs to set stream-output buffer offsets because applications can write to the *BufferFilledSize* with the CPU or GPU directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea24d-134">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ea24d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea24d-135">Zähler und Abfragen</span><span class="sxs-lookup"><span data-stu-id="ea24d-135">Counters and Queries</span></span>](counters-and-queries.md)
</dt> </dl>

 

 




