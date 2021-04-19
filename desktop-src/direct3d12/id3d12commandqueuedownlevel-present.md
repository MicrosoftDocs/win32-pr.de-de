---
title: ID3D12CommandQueueDownlevel::P Resent-Methode
description: Kopiert Inhalt aus einer Direct3D 12 Texture2D-Ressource in ein-Fenster. | ID3D12CommandQueueDownlevel::P Resent-Methode
keywords:
- Present-Methode
- Present-Methode, ID3D12CommandQueueDownlevel-Schnittstelle
- ID3D12CommandQueueDownlevel-Schnittstelle, Present-Methode
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350706"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a><span data-ttu-id="e2e7c-107">ID3D12CommandQueueDownlevel::P Resent-Methode</span><span class="sxs-lookup"><span data-stu-id="e2e7c-107">ID3D12CommandQueueDownlevel::Present method</span></span>

<span data-ttu-id="e2e7c-108">Kopiert Inhalt aus einer Direct3D 12 Texture2D-Ressource in ein-Fenster.</span><span class="sxs-lookup"><span data-stu-id="e2e7c-108">Copies contents from a Direct3D 12 Texture2D resource into a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e7c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2e7c-109">Syntax</span></span>

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a><span data-ttu-id="e2e7c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e7c-110">Parameters</span></span>

`pOpenCommandList`

<span data-ttu-id="e2e7c-111">Typ: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="e2e7c-111">Type: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="e2e7c-112">Eine geöffnete Befehlsliste, in der Direct3D 12 einen aktuellen Befehl in die Warteschlange einreiht und dann geschlossen und für Sie übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="e2e7c-112">An open command list, which Direct3D 12 enqueues a Present command onto, and then closes and submits for you.</span></span>

`pSourceTex2D`

<span data-ttu-id="e2e7c-113">Typ: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="e2e7c-113">Type: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="e2e7c-114">Eine Ressource mit den gewünschten Inhalten, die angezeigt werden sollen, mit Dimensions [**D3D12 \_ Resource \_ Dimension \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)und einem Format, das einer der folgenden ist.</span><span class="sxs-lookup"><span data-stu-id="e2e7c-114">A resource containing your desired contents to display, with dimension [**D3D12\_RESOURCE\_DIMENSION\_TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension), and a format that is one of the following.</span></span>

* <span data-ttu-id="e2e7c-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span><span class="sxs-lookup"><span data-stu-id="e2e7c-115">DXGI_FORMAT_R16G16B16A16_FLOAT</span></span>
* <span data-ttu-id="e2e7c-116">DXGI_FORMAT_R10G10B10A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="e2e7c-116">DXGI_FORMAT_R10G10B10A2_UNORM</span></span>
* <span data-ttu-id="e2e7c-117">DXGI_FORMAT_R8G8B8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="e2e7c-117">DXGI_FORMAT_R8G8B8A8_UNORM</span></span>
* <span data-ttu-id="e2e7c-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="e2e7c-118">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</span></span>
* <span data-ttu-id="e2e7c-119">DXGI_FORMAT_B8G8R8X8_UNORM</span><span class="sxs-lookup"><span data-stu-id="e2e7c-119">DXGI_FORMAT_B8G8R8X8_UNORM</span></span>
* <span data-ttu-id="e2e7c-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span><span class="sxs-lookup"><span data-stu-id="e2e7c-120">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</span></span>
* <span data-ttu-id="e2e7c-121">DXGI_FORMAT_B8G8R8A8_UNORM</span><span class="sxs-lookup"><span data-stu-id="e2e7c-121">DXGI_FORMAT_B8G8R8A8_UNORM</span></span>
* <span data-ttu-id="e2e7c-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span><span class="sxs-lookup"><span data-stu-id="e2e7c-122">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</span></span>

`hWindow`

<span data-ttu-id="e2e7c-123">Typ: **[HWND](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e2e7c-123">Type: **[HWND](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e2e7c-124">Das Handle für das Fenster, in dem der Inhalt angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2e7c-124">The handle to the window where the contents should be displayed.</span></span>

`Flags`

<span data-ttu-id="e2e7c-125">Type: **[D3D12 \_ Downlevel \_ Present \_ Flags](d3d12_downlevel_present_flags.md)**</span><span class="sxs-lookup"><span data-stu-id="e2e7c-125">Type: **[D3D12\_DOWNLEVEL\_PRESENT\_FLAGS](d3d12_downlevel_present_flags.md)**</span></span>

<span data-ttu-id="e2e7c-126">Flags zum Ändern des **aktuellen** Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="e2e7c-126">Flags to modify the **Present** operation.</span></span>

## <a name="return-value"></a><span data-ttu-id="e2e7c-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e7c-127">Return value</span></span>

<span data-ttu-id="e2e7c-128">Gibt bei Erfolg **S_OK** oder andernfalls ein fehlerhaftes HRESULT zurück.</span><span class="sxs-lookup"><span data-stu-id="e2e7c-128">Returns **S_OK** on success, or else a failing HRESULT.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e7c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2e7c-129">Requirements</span></span>

| <span data-ttu-id="e2e7c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2e7c-130">Requirement</span></span> | <span data-ttu-id="e2e7c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e2e7c-131">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="e2e7c-132">Header</span><span class="sxs-lookup"><span data-stu-id="e2e7c-132">Header</span></span> | <span data-ttu-id="e2e7c-133">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="e2e7c-133">d3d12downlevel.h</span></span> |
| <span data-ttu-id="e2e7c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e2e7c-134">DLL</span></span>    | <span data-ttu-id="e2e7c-135">D3D12.dll (nur Windows 7)</span><span class="sxs-lookup"><span data-stu-id="e2e7c-135">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e2e7c-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2e7c-136">See also</span></span>
* [<span data-ttu-id="e2e7c-137">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="e2e7c-137">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="e2e7c-138">Direct3D 12 auf Windows 7-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e2e7c-138">Direct3D 12 On Windows 7 interfaces</span></span>](direct3d-12on7-interfaces.md)
* [<span data-ttu-id="e2e7c-139">Referenz zu Direct3D 12 auf Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="e2e7c-139">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="e2e7c-140">Direct3D 12 unter Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2e7c-140">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
