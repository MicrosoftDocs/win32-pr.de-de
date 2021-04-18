---
description: Dieser Artikel enthält Anleitungen für die Bewegungsvektor Schätzung mit Direct3D 12-Video-APIs.
ms.assetid: ''
title: Direct3D-Video-Bewegungsschätzung
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 7fdb6146e1bb77c673eb89d944bcf42a8babce49
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "106365207"
---
# <a name="direct3d-video-motion-estimation"></a><span data-ttu-id="51dec-103">Direct3D-Video-Bewegungsschätzung</span><span class="sxs-lookup"><span data-stu-id="51dec-103">Direct3D video motion estimation</span></span>

<span data-ttu-id="51dec-104">Dieser Artikel enthält Anleitungen für die Bewegungsvektor Schätzung mit Direct3D 12-Video-APIs.</span><span class="sxs-lookup"><span data-stu-id="51dec-104">This article contains guidance for motion vector estimation with Direct3D 12 video APIs.</span></span> <span data-ttu-id="51dec-105">Diese Funktion wurde in Windows 10, Version 2004, eingeführt (10,0; Build 19041).</span><span class="sxs-lookup"><span data-stu-id="51dec-105">This feature was introduced in Windows 10, version 2004 (10.0; Build 19041).</span></span> <span data-ttu-id="51dec-106">Die Bewegungs Schätzung ist der Prozess der Bestimmung von Bewegungsvektoren, die die Transformation von einem 2D-Bild zu einem anderen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="51dec-106">Motion estimation is the process of determining motion vectors that describe the transformation from one 2D image to another.</span></span> <span data-ttu-id="51dec-107">Die Bewegungs Schätzung ist ein wesentlicher Bestandteil der Videocodierung und kann in Algorithmen zur Konvertierung von Frameraten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51dec-107">Motion estimation is an essential part of video encoding and can be used in frame rate conversion algorithms.</span></span> 

<span data-ttu-id="51dec-108">Obwohl die Bewegungs Schätzung mit Shadern implementiert werden kann, besteht der Zweck der D3D12 Motion-Schätzung darin, die Beschleunigung fester Funktionen für die Bewegungssuche verfügbar zu machen, um diesen Teil der Arbeit aus 3D zu laden.</span><span class="sxs-lookup"><span data-stu-id="51dec-108">While motion estimation can be implemented with shaders, the purpose of the D3D12 Motion Estimation feature is to expose fixed function acceleration for motion searching to offload this part of the work from 3D.</span></span> <span data-ttu-id="51dec-109">Dies hat häufig den Fall, dass die GPU-Video Encoder-Bewegungs Schätzung verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="51dec-109">Often this comes in the form of exposing the GPU video encoder motion estimator.</span></span> <span data-ttu-id="51dec-110">Das Ziel der D3D12 Motion-Schätzung ist ein optischer Fluss, aber beachten Sie, dass Encoder-Bewegungs Schätz Punkte für eine verbesserte Komprimierung optimiert werden können.</span><span class="sxs-lookup"><span data-stu-id="51dec-110">The goal of D3D12 Motion estimation is optical flow, but it should be noted that encoder motion estimators may be optimized for improving compression.</span></span>


## <a name="checking-for-support"></a><span data-ttu-id="51dec-111">Überprüfen der Unterstützung</span><span class="sxs-lookup"><span data-stu-id="51dec-111">Checking for Support</span></span>

<span data-ttu-id="51dec-112">Bestimmen Sie die Unterstützung für alle D3D-Video Features durch Aufrufen von [ID3D12VideoDevice:: checkfeaturesupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) , und übergeben Sie einen Wert aus der [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) -Enumeration, um das Feature anzugeben, für das die Unterstützung abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="51dec-112">Determine support for all D3D video features by calling [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) and passing in a value from the [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify the feature for which support is being queried.</span></span> <span data-ttu-id="51dec-113">Um die unterstützte Blockgröße und Auflösungen für ein bestimmtes Format abzufragen, verwenden Sie den **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** Wert, und geben Sie eine [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) Struktur für *pfeaturesupportdata* an, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="51dec-113">To query the supported block size and resolutions for a given format, use the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** value and supply a [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) structure for the *pFeatureSupportData* as shown in the example below.</span></span> <span data-ttu-id="51dec-114">In der aktuellen Version wird nur **DXGI_FORMAT_NV12** unterstützt, daher müssen Inhalte in anderen Formaten farblich konvertiert und herabgestuft werden, damit die Bewegungs Schätzung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="51dec-114">In the current release, only **DXGI_FORMAT_NV12** is supported, so content in other formats may need to be color converted and downsampled to use motion estimation.</span></span>

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a><span data-ttu-id="51dec-115">Das Bewegungs Schätz Kontext Objekt</span><span class="sxs-lookup"><span data-stu-id="51dec-115">The motion estimator context object</span></span>

<span data-ttu-id="51dec-116">Das [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) -Objekt verwaltet den Kontext für videobewegungs-Schätz Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="51dec-116">The [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) object maintains context for video motion estimation operations.</span></span> <span data-ttu-id="51dec-117">Erstellen Sie eine neue Instanz dieser Schnittstelle durch Aufrufen von [ID3D12VideoDevice1:: createvideomotionestimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span><span class="sxs-lookup"><span data-stu-id="51dec-117">Create a new instance of this interface by calling [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span></span>

<span data-ttu-id="51dec-118">Die ausgewählte Blockgröße, Genauigkeit und der unterstützte Größenbereich hängen von den Werten ab, die von der von der **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** -Funktionsüberprüfung zurückgegebenen Hardware unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="51dec-118">The selected block size, precision, and supported size range would depend on values supported by hardware returned from the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** feature check.</span></span> <span data-ttu-id="51dec-119">Sie können einen kleineren Größenbereich auswählen, der vom Treiber unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="51dec-119">You can select a smaller size range than the driver supports.</span></span> <span data-ttu-id="51dec-120">Der Größenbereich informiert die internen Zuordnungs Größen.</span><span class="sxs-lookup"><span data-stu-id="51dec-120">Size range informs internal allocation sizes.</span></span>

```c++
D3D12_VIDEO_MOTION_ESTIMATOR_DESC motionEstimatorDesc = { 
    0, //NodeIndex
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionEstimator> spVideoMotionEstimator;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionEstimator(
    &motionEstimatorDesc, 
    nullptr,
    IID_PPV_ARGS(&spVideoMotionEstimator)));
```



## <a name="storage-of-motion-vectors"></a><span data-ttu-id="51dec-121">Speicherung von Bewegungsvektoren</span><span class="sxs-lookup"><span data-stu-id="51dec-121">Storage of motion vectors</span></span>

<span data-ttu-id="51dec-122">Der [ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) speichert Bewegungsvektoren.</span><span class="sxs-lookup"><span data-stu-id="51dec-122">The [ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) stores motion vectors.</span></span> <span data-ttu-id="51dec-123">Diese Schnittstelle wird von der [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) Struktur verwendet, die von [ID3D12VideoEncodeCommandList:: estimatemotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="51dec-123">This interface is used by the [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) structure returned from [ID3D12VideoEncodeCommandList::EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion).</span></span> <span data-ttu-id="51dec-124">Die aufgelöste 2D-Textur der Ausgabe ist eine [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Textur, bei der R die horizontale Komponente enthält und G die vertikale Komponente des Bewegungs Vektors enthält.</span><span class="sxs-lookup"><span data-stu-id="51dec-124">The resolved output 2D texture is a [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) texture where R holds the horizontal component and G holds the vertical component of the motion vector.</span></span> <span data-ttu-id="51dec-125">Diese Textur ist so groß, dass ein Komponenten Paar pro Block enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="51dec-125">This texture is sized to hold one pair of components per block.</span></span> <span data-ttu-id="51dec-126">Mit [ID3D12VideoEncodeCommandList:: resolvemuvetorheap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) wird die Bewegungsvektor Ausgabe von **estimatemotion** von Hardware abhängigen Formaten in ein konsistentes Format übersetzt, das von den APIs für die Video Bewegungs Schätzung definiert wird.</span><span class="sxs-lookup"><span data-stu-id="51dec-126">Call [ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) to translates the motion vector output of **EstimateMotion** from hardware-dependent formats into a consistent format defined by the video motion estimation APIs.</span></span>

```c++
D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC MotionVectorHeapDesc = { 
    0, // NodeIndex 
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionVectorHeap> spVideoMotionVectorHeap;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionVectorHeap(
    &MotionVectorHeapDesc, 
    nullptr, 
    IID_PPV_ARGS(&spVideoMotionVectorHeap)));
```

```cpp
    CD3DX12_RESOURCE_DESC::Tex2D(
        DXGI_FORMAT_R16G16_SINT, 
        Align(1920, 16) / 16, // This example uses a 16x16 block size. Pixel width and height
        Align(1080, 16) / 16, // are adjusted to store the vectors for those blocks.
        1, // ArraySize
        1  // MipLevels
        );

    ATL::CComPtr< ID3D12Resource > spResolvedMotionVectors;
    VERIFY_SUCCEEDED(pDevice->CreateCommittedResource(
        &Properties,
        D3D12_HEAP_FLAG_NONE,
        &resolvedMotionVectorDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        IID_PPV_ARGS(&spResolvedMotionVectors)));
```

 <span data-ttu-id="51dec-127">**ID3D12VideoMotionVectorHeap** wird auch verwendet, um Hinweis Vektoren in der [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) Struktur bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="51dec-127">**ID3D12VideoMotionVectorHeap** is also used to supply hint vectors in the [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) structure.</span></span>



## <a name="estimate-motion-in-a-command-list"></a><span data-ttu-id="51dec-128">Bewegung in einer Befehlsliste schätzen</span><span class="sxs-lookup"><span data-stu-id="51dec-128">Estimate motion in a command list</span></span>

<span data-ttu-id="51dec-129">Rufen Sie die [estimatemotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) aus einem [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) auf, um den Vorgang der Bewegungs Schätzung aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="51dec-129">Call the [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) from a [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) to invoke the motion estimation operation.</span></span>

<span data-ttu-id="51dec-130">Im folgenden Beispiel wird die Motion-Suche ausgeführt, und die Bewegungsvektoren werden mit [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)in die 2D-Textur aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="51dec-130">The example below executes the motion search and resolves the motion vectors to the 2D texture with [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>  <span data-ttu-id="51dec-131">D3D12-Ressourcen, die als Eingabe für **estimatemotion** verwendet werden, müssen sich im [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) Zustand befinden, und die Ressource, in die von **resolvemutionvectorheap** geschrieben wird, muss sich im Status [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) befinden.</span><span class="sxs-lookup"><span data-stu-id="51dec-131">D3D12 Resources used as input to **EstimateMotion** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state and the resource written to by **ResolveMotionVectorHeap** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state.</span></span>

```cpp
const D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT outputArgs = {spVideoMotionVectorHeap};

const D3D12_VIDEO_MOTION_ESTIMATOR_INPUT inputArgs = {
    spCurrentResource,
    0,
    spReferenceResource,
    0,
    nullptr // pHintMotionVectorHeap
    };

spCommandList->EstimateMotion(spVideoMotionEstimator, &outputArgs, &inputArgs);

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT outputArgs = { 
    spResolvedMotionVectors,
    {}};

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT inputArgs = {
    spVideoMotionVectorHeap,
    1920,
    1080
    };

spCommandList->ResolveMotionVectorHeap(&outputArgs, &inputArgs);
        
VERIFY(spCommandList->Close());

// Execute Commandlist.
ID3D12CommandList *ppCommandLists[1] = { spCommandList.p };
spCommandQueue->ExecuteCommandLists(1, ppCommandLists);
```


## <a name="protected-resources"></a><span data-ttu-id="51dec-132">Geschützte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="51dec-132">Protected resources</span></span>

<span data-ttu-id="51dec-133">Die Direct3D 12 Motion Vector-Schätzung unterstützt das Lesen und Schreiben von Hardware-DRM-geschützten Ressourcen, wenn Sie vom Treiber unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="51dec-133">Direct3D 12 motion vector estimation supports reading from and writing to hardware DRM protected resources when supported by the driver.</span></span> <span data-ttu-id="51dec-134">Wenn die Eingabe Ressourcen Hardware-DRM-geschützt sind, ist die Ausgabe auch eine durch Hardware DRM geschützte Ressource. Die Methoden, die zum Erstellen des Kontext Objekts der Bewegungs Schätzung und des Motion Vector Heap,  [ID3D12VideoDevice1:: createvideomotionestimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) und [ID3D12VideoDevice1:: createvideomotionvectorheap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap)verwendet wurden, akzeptieren beide ein [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) -Objekt, das zum Verwalten des Zugriffs auf geschützte Ressourcen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51dec-134">If the input resources are hardware DRM protected, the output is also a hardware DRM protected resource.The methods used to create the motion estimation context object and the motion vector heap,  [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) and [ID3D12VideoDevice1::CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), both accept a [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) that is used to manage access to protected resources.</span></span> 

<span data-ttu-id="51dec-135">Verwenden Sie [ID3D12VideoMotionEstimator:: getprotectedresourcesession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) und [ID3D12VideoMotionVectorHeap:: getprotectedresourcesession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) , um die **ID3D12ProtectedResourceSession** -Objekte abzurufen, die bereitgestellt wurden, als die Objekte erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="51dec-135">Use [ID3D12VideoMotionEstimator::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) and [ID3D12VideoMotionVectorHeap::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) to retrieve the **ID3D12ProtectedResourceSession** objects provided when the objects were created.</span></span>



## <a name="related-topics"></a><span data-ttu-id="51dec-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51dec-136">Related topics</span></span>

* [<span data-ttu-id="51dec-137">Direct3D 12-Video-APIs</span><span class="sxs-lookup"><span data-stu-id="51dec-137">Direct3D 12 Video APIs</span></span>](direct3d-12-video-apis.md)
* [<span data-ttu-id="51dec-138">Media Foundation-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="51dec-138">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
