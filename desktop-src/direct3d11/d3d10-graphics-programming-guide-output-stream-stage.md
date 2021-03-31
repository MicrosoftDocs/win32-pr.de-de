---
title: Stream-Output Phase
description: Der Zweck der Stream-Output-Phase besteht darin, Vertexdaten fortlaufend aus der Geometrie-Shader-Stufe (oder der Vertex-Shader-Phase, wenn die Geometrie-shaderstufe inaktiv ist) in einen oder mehrere Puffer im Arbeitsspeicher auszugeben (oder zu streamen) (Weitere Informationen finden Sie unter Getting Started with the Stream-Output Stage).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- Stream-Ausgabestufe (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0879cde2ba2f1bb3ed9cc6121aaf378cd4af312
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474685"
---
# <a name="stream-output-stage"></a><span data-ttu-id="555bb-104">Stream-Output Phase</span><span class="sxs-lookup"><span data-stu-id="555bb-104">Stream-Output Stage</span></span>

<span data-ttu-id="555bb-105">Der Zweck der Stream-Output-Phase besteht darin, Vertexdaten fortlaufend aus der Geometrie-Shader-Stufe (oder der Vertex-Shader-Phase, wenn die Geometrie-shaderstufe inaktiv ist) in einen oder mehrere Puffer im Arbeitsspeicher auszugeben (oder zu streamen) (Weitere Informationen finden Sie unter [Getting Started with the Stream-Output Stage](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span><span class="sxs-lookup"><span data-stu-id="555bb-105">The purpose of the stream-output stage is to continuously output (or stream) vertex data from the geometry-shader stage (or the vertex-shader stage if the geometry-shader stage is inactive) to one or more buffers in memory (see [Getting Started with the Stream-Output Stage](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span></span>

<span data-ttu-id="555bb-106">Die Stream-Output-Phase (also) befindet sich in der Pipeline direkt hinter der Geometrie-Shader-Phase und unmittelbar vor der rasterisierungsphase, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="555bb-106">The stream-output stage (SO) is located in the pipeline right after the geometry-shader stage and just before the rasterization stage, as shown in the following diagram.</span></span>

![Diagramm des Speicher Orts der Stream-Ausgabestufe in der Pipeline](images/d3d10-pipeline-stages-so.png)

<span data-ttu-id="555bb-108">Daten, die in den Arbeitsspeicher gestreamt werden, können in einem nachfolgenden Renderingdurchlauf wieder in die Pipeline eingelesen werden oder in eine stagingressource kopiert werden (damit Sie von der CPU gelesen werden kann).</span><span class="sxs-lookup"><span data-stu-id="555bb-108">Data streamed out to memory can be read back into the pipeline in a subsequent rendering pass, or can be copied to a staging resource (so it can be read by the CPU).</span></span> <span data-ttu-id="555bb-109">Die Menge der Daten, die gestreamt werden, kann variieren. die [**Verknüpfung id3d11devicecontext aus::D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) -API ist so konzipiert, dass die Daten verarbeitet werden, ohne dass die Menge der geschriebenen Daten (GPU) abgefragt werden muss.</span><span class="sxs-lookup"><span data-stu-id="555bb-109">The amount of data streamed out can vary; the [**ID3D11DeviceContext::DrawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) API is designed to handle the data without the need to query (the GPU) about the amount of data written.</span></span>

<span data-ttu-id="555bb-110">Wenn ein Dreieck oder ein Zeilen Streifen an die Eingabe-Assembler-Phase gebunden ist, wird jeder Strip in eine Liste konvertiert, bevor diese gestreamt werden. Scheitel Punkte werden immer als umfassende primitive geschrieben (z. b. 3 Scheitel Punkte gleichzeitig für Dreiecke); unvollständige primitive werden niemals gestreamt. Primitive Typen mit der Konsistenz verwerfen vor dem Streamen von Daten die Daten der Daten.</span><span class="sxs-lookup"><span data-stu-id="555bb-110">When a triangle or line strip is bound to the input-assembler stage, each strip is converted into a list before they are streamed out. Vertices are always written out as complete primitives (for example, 3 vertices at a time for triangles); incomplete primitives are never streamed out. Primitive types with adjacency discard the adjacency data before streaming data out.</span></span>

<span data-ttu-id="555bb-111">Es gibt zwei Möglichkeiten, Datenstrom Ausgabedaten in die Pipeline zu übermitteln:</span><span class="sxs-lookup"><span data-stu-id="555bb-111">There are two ways to feed stream-output data into the pipeline:</span></span>

-   <span data-ttu-id="555bb-112">Stream-Ausgabedaten können wieder in die Eingabe-Assembler-Phase eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="555bb-112">Stream-output data can be fed back into the input-assembler stage.</span></span>
-   <span data-ttu-id="555bb-113">Stream-Ausgabedaten können von programmierbaren Shadern mithilfe von Ladefunktionen (z. b. [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)) gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="555bb-113">Stream-output data can be read by programmable shaders using load functions (such as [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span></span>

<span data-ttu-id="555bb-114">Wenn Sie einen Puffer als Stream-Output-Ressource verwenden möchten, erstellen Sie den Puffer mit dem [**D3D11 \_ Bind- \_ \_ Ausgabe**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="555bb-114">To use a buffer as a stream-output resource, create the buffer with the [**D3D11\_BIND\_STREAM\_OUTPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) flag.</span></span> <span data-ttu-id="555bb-115">Die Stream-Output-Stufe unterstützt bis zu 4 Puffer gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="555bb-115">The stream-output stage supports up to 4 buffers simultaneously.</span></span>

-   <span data-ttu-id="555bb-116">Wenn Sie Daten in mehrere Puffer streamen, kann jeder Puffer nur ein einzelnes Element (bis zu 4 Komponenten) von pro-Vertex-Daten erfassen, wobei ein impliziter Daten Sprung gleich der Elementbreite in den einzelnen Puffern ist (kompatibel mit der Art und Weise, wie einzelne Element Puffer für Eingaben in Shader-Stufen gebunden werden können).</span><span class="sxs-lookup"><span data-stu-id="555bb-116">If you are streaming data into multiple buffers, each buffer can only capture a single element (up to 4 components) of per-vertex data, with an implied data stride equal to the element width in each buffer (compatible with the way single element buffers can be bound for input into shader stages).</span></span> <span data-ttu-id="555bb-117">Wenn die Puffer über unterschiedliche Größen verfügen, wird der Schreibvorgang beendet, sobald ein Puffer voll ist.</span><span class="sxs-lookup"><span data-stu-id="555bb-117">Furthermore, if the buffers have different sizes, writing stops as soon as any one of the buffers is full.</span></span>
-   <span data-ttu-id="555bb-118">Wenn Sie Daten in einen einzelnen Puffer streamen, kann der Puffer bis zu 64 skalare Komponenten von pro-Vertex-Daten (256 Bytes oder weniger) erfassen, oder der Scheitelpunkt Schritt kann bis zu 2048 Byte betragen.</span><span class="sxs-lookup"><span data-stu-id="555bb-118">If you are streaming data into a single buffer, the buffer can capture up to 64 scalar components of per-vertex data (256 bytes or less) or the vertex stride can be up to 2048 bytes.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="555bb-119">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="555bb-119">In this section</span></span>



| <span data-ttu-id="555bb-120">Thema</span><span class="sxs-lookup"><span data-stu-id="555bb-120">Topic</span></span>                                                                                                                               | <span data-ttu-id="555bb-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="555bb-121">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="555bb-122">Ersten Einstieg in die Stream-Output Phase</span><span class="sxs-lookup"><span data-stu-id="555bb-122">Getting Started with the Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | <span data-ttu-id="555bb-123">In diesem Abschnitt wird beschrieben, wie ein Geometry-Shader mit der Stream-Ausgabestufe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="555bb-123">This section describes how to use a geometry shader with the stream output stage.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="555bb-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="555bb-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="555bb-125">Grafik Pipeline</span><span class="sxs-lookup"><span data-stu-id="555bb-125">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="555bb-126">Pipeline Stufen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="555bb-126">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

