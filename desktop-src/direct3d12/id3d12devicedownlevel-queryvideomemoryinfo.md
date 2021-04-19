---
title: 'ID3D12DeviceDownlevel:: queryvideomemoryinfo-Methode'
description: 'Kopiert Inhalt aus einer Direct3D 12 Texture2D-Ressource in ein-Fenster. | ID3D12DeviceDownlevel:: queryvideomemoryinfo-Methode'
keywords:
- Queryvideomemoryinfo-Methode
- Queryvideomemoryinfo-Methode, ID3D12DeviceDownlevel-Schnittstelle
- ID3D12DeviceDownlevel Interface, queryvideomemoryinfo-Methode
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 32b93fcbbe44aaae0916e6d8f3f403eb960e26eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355214"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a><span data-ttu-id="ab5a0-107">ID3D12DeviceDownlevel:: queryvideomemoryinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="ab5a0-107">ID3D12DeviceDownlevel::QueryVideoMemoryInfo method</span></span>

<span data-ttu-id="ab5a0-108">Stellt Arbeitsspeicher Statistiken für Windows 7 bereit.</span><span class="sxs-lookup"><span data-stu-id="ab5a0-108">Provides memory statistics on Windows 7.</span></span> <span data-ttu-id="ab5a0-109">Diese Methode entspricht [IDXGIAdapter3:: queryvideomemoryinfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), die unter Windows 7 nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ab5a0-109">This method is equivalent to [IDXGIAdapter3::QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo), which is not available on Windows 7.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab5a0-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab5a0-110">Syntax</span></span>

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a><span data-ttu-id="ab5a0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab5a0-111">Parameters</span></span>

`NodeIndex`

<span data-ttu-id="ab5a0-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="ab5a0-112">Type: **UINT**</span></span>

<span data-ttu-id="ab5a0-113">Gibt den physischen Adapter des Geräts an, für den die Informationen zum Videospeicher abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="ab5a0-113">Specifies the device's physical adapter for which the video memory information is queried.</span></span> <span data-ttu-id="ab5a0-114">Legen Sie für einen Single-GPU-Vorgang NULL fest.</span><span class="sxs-lookup"><span data-stu-id="ab5a0-114">For single-GPU operation, set this to zero.</span></span> <span data-ttu-id="ab5a0-115">Wenn mehrere GPU-Knoten vorhanden sind, legen Sie diese auf den Index des Knotens (den physischen Adapter des Geräts) fest, für den die Informationen zum Videospeicher abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="ab5a0-115">If there are multiple GPU nodes, set this to the index of the node (the device's physical adapter) for which the video memory information is queried.</span></span> <span data-ttu-id="ab5a0-116">Weitere Informationen finden Sie unter [multiadaptersysteme](multi-engine.md).</span><span class="sxs-lookup"><span data-stu-id="ab5a0-116">See [Multi-adapter systems](multi-engine.md).</span></span>

`MemorySegmentGroup`

<span data-ttu-id="ab5a0-117">Typ: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span><span class="sxs-lookup"><span data-stu-id="ab5a0-117">Type: **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**</span></span>

<span data-ttu-id="ab5a0-118">Gibt eine **DXGI_MEMORY_SEGMENT_GROUP** an, die die Gruppe als lokal oder nicht lokal identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ab5a0-118">Specifies a **DXGI_MEMORY_SEGMENT_GROUP** that identifies the group as local or non-local.</span></span>

`pVideoMemoryInfo`

<span data-ttu-id="ab5a0-119">Typ: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span><span class="sxs-lookup"><span data-stu-id="ab5a0-119">Type: **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***</span></span>

<span data-ttu-id="ab5a0-120">Füllt eine **DXGI_QUERY_VIDEO_MEMORY_INFO** Struktur mit den aktuellen Werten aus.</span><span class="sxs-lookup"><span data-stu-id="ab5a0-120">Fills in a **DXGI_QUERY_VIDEO_MEMORY_INFO** structure with the current values.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab5a0-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab5a0-121">Return value</span></span>

<span data-ttu-id="ab5a0-122">Gibt bei Erfolg **S_OK** oder andernfalls ein fehlerhaftes HRESULT zurück.</span><span class="sxs-lookup"><span data-stu-id="ab5a0-122">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab5a0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab5a0-123">Requirements</span></span>

| <span data-ttu-id="ab5a0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab5a0-124">Requirement</span></span> | <span data-ttu-id="ab5a0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ab5a0-125">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="ab5a0-126">Header</span><span class="sxs-lookup"><span data-stu-id="ab5a0-126">Header</span></span> | <span data-ttu-id="ab5a0-127">d3d12downlevel. h und dxgi1_4. h</span><span class="sxs-lookup"><span data-stu-id="ab5a0-127">d3d12downlevel.h and dxgi1_4.h</span></span> |
| <span data-ttu-id="ab5a0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ab5a0-128">DLL</span></span>    | <span data-ttu-id="ab5a0-129">D3D12.dll (nur Windows 7)</span><span class="sxs-lookup"><span data-stu-id="ab5a0-129">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ab5a0-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab5a0-130">See also</span></span>
* [<span data-ttu-id="ab5a0-131">ID3D12DeviceDownlevel</span><span class="sxs-lookup"><span data-stu-id="ab5a0-131">ID3D12DeviceDownlevel</span></span>](id3d12devicedownlevel.md)
* [<span data-ttu-id="ab5a0-132">Direct3D 12 auf Windows 7-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ab5a0-132">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="ab5a0-133">Referenz zu Direct3D 12 auf Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="ab5a0-133">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="ab5a0-134">Direct3D 12 unter Windows 7</span><span class="sxs-lookup"><span data-stu-id="ab5a0-134">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
