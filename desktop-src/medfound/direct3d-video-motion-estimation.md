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
# <a name="direct3d-video-motion-estimation"></a>Direct3D-Video-Bewegungsschätzung

Dieser Artikel enthält Anleitungen für die Bewegungsvektor Schätzung mit Direct3D 12-Video-APIs. Diese Funktion wurde in Windows 10, Version 2004, eingeführt (10,0; Build 19041). Die Bewegungs Schätzung ist der Prozess der Bestimmung von Bewegungsvektoren, die die Transformation von einem 2D-Bild zu einem anderen beschreiben. Die Bewegungs Schätzung ist ein wesentlicher Bestandteil der Videocodierung und kann in Algorithmen zur Konvertierung von Frameraten verwendet werden. 

Obwohl die Bewegungs Schätzung mit Shadern implementiert werden kann, besteht der Zweck der D3D12 Motion-Schätzung darin, die Beschleunigung fester Funktionen für die Bewegungssuche verfügbar zu machen, um diesen Teil der Arbeit aus 3D zu laden. Dies hat häufig den Fall, dass die GPU-Video Encoder-Bewegungs Schätzung verfügbar gemacht wird. Das Ziel der D3D12 Motion-Schätzung ist ein optischer Fluss, aber beachten Sie, dass Encoder-Bewegungs Schätz Punkte für eine verbesserte Komprimierung optimiert werden können.


## <a name="checking-for-support"></a>Überprüfen der Unterstützung

Bestimmen Sie die Unterstützung für alle D3D-Video Features durch Aufrufen von [ID3D12VideoDevice:: checkfeaturesupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) , und übergeben Sie einen Wert aus der [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) -Enumeration, um das Feature anzugeben, für das die Unterstützung abgefragt wird. Um die unterstützte Blockgröße und Auflösungen für ein bestimmtes Format abzufragen, verwenden Sie den **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** Wert, und geben Sie eine [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) Struktur für *pfeaturesupportdata* an, wie im folgenden Beispiel gezeigt. In der aktuellen Version wird nur **DXGI_FORMAT_NV12** unterstützt, daher müssen Inhalte in anderen Formaten farblich konvertiert und herabgestuft werden, damit die Bewegungs Schätzung verwendet werden kann.

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a>Das Bewegungs Schätz Kontext Objekt

Das [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) -Objekt verwaltet den Kontext für videobewegungs-Schätz Vorgänge. Erstellen Sie eine neue Instanz dieser Schnittstelle durch Aufrufen von [ID3D12VideoDevice1:: createvideomotionestimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).

Die ausgewählte Blockgröße, Genauigkeit und der unterstützte Größenbereich hängen von den Werten ab, die von der von der **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** -Funktionsüberprüfung zurückgegebenen Hardware unterstützt werden. Sie können einen kleineren Größenbereich auswählen, der vom Treiber unterstützt wird. Der Größenbereich informiert die internen Zuordnungs Größen.

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



## <a name="storage-of-motion-vectors"></a>Speicherung von Bewegungsvektoren

Der [ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) speichert Bewegungsvektoren. Diese Schnittstelle wird von der [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) Struktur verwendet, die von [ID3D12VideoEncodeCommandList:: estimatemotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion)zurückgegeben wird. Die aufgelöste 2D-Textur der Ausgabe ist eine [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Textur, bei der R die horizontale Komponente enthält und G die vertikale Komponente des Bewegungs Vektors enthält. Diese Textur ist so groß, dass ein Komponenten Paar pro Block enthalten ist. Mit [ID3D12VideoEncodeCommandList:: resolvemuvetorheap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) wird die Bewegungsvektor Ausgabe von **estimatemotion** von Hardware abhängigen Formaten in ein konsistentes Format übersetzt, das von den APIs für die Video Bewegungs Schätzung definiert wird.

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

 **ID3D12VideoMotionVectorHeap** wird auch verwendet, um Hinweis Vektoren in der [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) Struktur bereitzustellen.



## <a name="estimate-motion-in-a-command-list"></a>Bewegung in einer Befehlsliste schätzen

Rufen Sie die [estimatemotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) aus einem [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) auf, um den Vorgang der Bewegungs Schätzung aufzurufen.

Im folgenden Beispiel wird die Motion-Suche ausgeführt, und die Bewegungsvektoren werden mit [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)in die 2D-Textur aufgelöst.  D3D12-Ressourcen, die als Eingabe für **estimatemotion** verwendet werden, müssen sich im [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) Zustand befinden, und die Ressource, in die von **resolvemutionvectorheap** geschrieben wird, muss sich im Status [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) befinden.

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


## <a name="protected-resources"></a>Geschützte Ressourcen

Die Direct3D 12 Motion Vector-Schätzung unterstützt das Lesen und Schreiben von Hardware-DRM-geschützten Ressourcen, wenn Sie vom Treiber unterstützt werden. Wenn die Eingabe Ressourcen Hardware-DRM-geschützt sind, ist die Ausgabe auch eine durch Hardware DRM geschützte Ressource. Die Methoden, die zum Erstellen des Kontext Objekts der Bewegungs Schätzung und des Motion Vector Heap,  [ID3D12VideoDevice1:: createvideomotionestimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) und [ID3D12VideoDevice1:: createvideomotionvectorheap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap)verwendet wurden, akzeptieren beide ein [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) -Objekt, das zum Verwalten des Zugriffs auf geschützte Ressourcen verwendet wird. 

Verwenden Sie [ID3D12VideoMotionEstimator:: getprotectedresourcesession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) und [ID3D12VideoMotionVectorHeap:: getprotectedresourcesession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) , um die **ID3D12ProtectedResourceSession** -Objekte abzurufen, die bereitgestellt wurden, als die Objekte erstellt wurden.



## <a name="related-topics"></a>Zugehörige Themen

* [Direct3D 12-Video-APIs](direct3d-12-video-apis.md)
* [Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md)
