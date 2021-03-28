---
title: Indizieren mehrerer Ausgabedaten Ströme
description: In Shader Model 5 kann ein Geometry-Shader bis zu 4 separate Streams unterstützen. Dies bedeutet, dass ein einzelner Shader abhängig von der Anzahl der deklarierten Streams zwischen einem und vier Ausgabestreams ausgeben kann.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8564917be9565e862043e370840f8ac7280f174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036435"
---
# <a name="how-to-index-multiple-output-streams"></a><span data-ttu-id="58261-104">Vorgehensweise: Indizieren mehrerer Ausgabedaten Ströme</span><span class="sxs-lookup"><span data-stu-id="58261-104">How To: Index Multiple Output Streams</span></span>

<span data-ttu-id="58261-105">In Shader Model 5 kann ein Geometry-Shader bis zu 4 separate Streams unterstützen.</span><span class="sxs-lookup"><span data-stu-id="58261-105">In shader model 5, a geometry shader can support up to 4 separate streams.</span></span> <span data-ttu-id="58261-106">Dies bedeutet, dass ein einzelner Shader abhängig von der Anzahl der deklarierten Streams zwischen einem und vier Ausgabestreams ausgeben kann.</span><span class="sxs-lookup"><span data-stu-id="58261-106">This means a single shader can output between one and four output streams, depending on the number of streams declared.</span></span>

<span data-ttu-id="58261-107">So indizieren Sie mehrere Ausgabedaten Ströme</span><span class="sxs-lookup"><span data-stu-id="58261-107">To index multiple output streams</span></span>

1.  <span data-ttu-id="58261-108">Definieren Sie einen Datenstrom mithilfe eines Datenstrom-Vorlagen Typs.</span><span class="sxs-lookup"><span data-stu-id="58261-108">Define a data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  <span data-ttu-id="58261-109">Definieren Sie einen zweiten Datenstrom mithilfe eines Stream-Vorlagen Typs.</span><span class="sxs-lookup"><span data-stu-id="58261-109">Define a second data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  <span data-ttu-id="58261-110">Ausgabedaten an Datenströme (oder beides) mithilfe der systeminternen Funktionen des Stream-Ausgabe Objekts (z. b. Append oder restartstrip).</span><span class="sxs-lookup"><span data-stu-id="58261-110">Output data to either (or both) streams using the stream output object intrinsic functions (such as Append or RestartStrip).</span></span>

    ```
    void MyGS( 
        InVertex verts[2], 
        inout PointStream<OutVertex1> myStream1, 
        inout PointStream<OutVertex2> myStream2 )
    {
        OutVertex1 myVert1 = TransformVertex1( verts[0] );
        OutVertex2 myVert2 = TransformVertex2( verts[1] );
        myStream1.Append( myVert1 );
        myStream2.Append( myVert2 );
    }
    ```

    

<span data-ttu-id="58261-111">Wenn Sie einen einzelnen Ausgabestream verwenden, können Sie Dreiecks Streifen, Zeilen Streifen oder Punkt Listen ausgeben.</span><span class="sxs-lookup"><span data-stu-id="58261-111">When using a single output stream, you can emit triangle strips, line strips, or point lists.</span></span> <span data-ttu-id="58261-112">Wenn Sie Dreieck-und Zeilen Streifen im Stream-out-Puffer speichern, werden Sie auf Dreieck-bzw. Zeilen Listen erweitert.</span><span class="sxs-lookup"><span data-stu-id="58261-112">When you store triangle and line strips in the stream out buffer, they are expanded to triangle and line lists respectively.</span></span> <span data-ttu-id="58261-113">Sie können auch einen Datenstrom Rasterisieren und ihn nicht an einen Arbeitsspeicher Puffer senden.</span><span class="sxs-lookup"><span data-stu-id="58261-113">You can also rasterize one stream and not send it to a memory buffer.</span></span>

<span data-ttu-id="58261-114">Bei der Verwendung mehrerer Ausgabedaten Ströme müssen alle Streams Punkte enthalten, und es kann bis zu einem Ausgabedatenstrom an den Rasterizer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="58261-114">When using multiple output streams, all streams must contain points, and up to one output stream can be sent to the rasterizer.</span></span> <span data-ttu-id="58261-115">Üblicherweise wird ein beliebiger Stream von einer Anwendung nicht rasterisiert.</span><span class="sxs-lookup"><span data-stu-id="58261-115">More commonly, an application will not rasterize any stream.</span></span>

<span data-ttu-id="58261-116">Nachdem Sie Daten in einen Puffer gestreamt haben, können Sie diese Daten verwenden, um jeden primitiven Typ zu erzeugen, nicht nur den primitiven Typ, den Sie zum Ausfüllen des Puffers verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="58261-116">After you stream data to a buffer, you can use that data to render any primitive type, not just the primitive type that you used to fill the buffer.</span></span>

<span data-ttu-id="58261-117">Die Gesamtausgabe des Geometry-Shaders ist auf 1024 skalare beschränkt.</span><span class="sxs-lookup"><span data-stu-id="58261-117">The total output of the geometry shader is limited to 1024 scalars.</span></span> <span data-ttu-id="58261-118">Wenn mehrere Streams vorhanden sind, wird die Anzahl der skalare aus dem größten Streamtyp multipliziert mit der maximalen Vertex-Anzahl berechnet.</span><span class="sxs-lookup"><span data-stu-id="58261-118">When multiple streams exist, the number of scalars is computed from the largest stream type multiplied by the maximum vertex count.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="58261-119">Unterschiede zwischen Shader-Modell 4 und Shader-Modell 5:</span><span class="sxs-lookup"><span data-stu-id="58261-119">Differences between shader model 4 and shader model 5:</span></span><br/> <span data-ttu-id="58261-120">Shadermodell 4:</span><span class="sxs-lookup"><span data-stu-id="58261-120">Shader model 4:</span></span><br/>
<ul>
<li><span data-ttu-id="58261-121">Die maximale Anzahl von skalaren für die Streamausgabe beträgt 64.</span><span class="sxs-lookup"><span data-stu-id="58261-121">Maximum number of scalars for stream output is 64.</span></span></li>
<li><span data-ttu-id="58261-122">Die Registrierungs Maske pro Komponente muss über den Index Bereich abgestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="58261-122">The per-component register mask must match across the index range.</span></span></li>
</ul>
<span data-ttu-id="58261-123">Shader-Modell 5:</span><span class="sxs-lookup"><span data-stu-id="58261-123">Shader model 5:</span></span><br/>
<ul>
<li><span data-ttu-id="58261-124">Die maximale Anzahl von skalaren für die Streamausgabe beträgt 128.</span><span class="sxs-lookup"><span data-stu-id="58261-124">Maximum number of scalars for stream output is 128.</span></span></li>
<li><span data-ttu-id="58261-125">Die Registrierungs Maske pro Komponente muss nicht über den Index Bereich abgestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="58261-125">The per-component register mask does not need to match across the index range.</span></span></li>
<li><span data-ttu-id="58261-126">Die dynamische Indizierung von Ausgaben muss für alle Streams rechtmäßig sein.</span><span class="sxs-lookup"><span data-stu-id="58261-126">Dynamic indexing of outputs must be legal across all streams.</span></span></li>
<li><span data-ttu-id="58261-127">Der Interpolations Modus muss für die Streams nicht abgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="58261-127">Interpolation modes do not need to match for the streams.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="58261-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58261-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58261-129">Geometry-Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="58261-129">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





