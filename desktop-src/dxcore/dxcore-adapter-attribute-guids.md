---
title: DXCore-Adapterattribut-GUIDs
description: 'Die folgenden Adapter Attribut-GUIDs werden in deklariert `dxcore_interface.h` und mit den [idxcoreadapterfactory:: deateadapterlist](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) -und [idxcoreadapter:: isattributesupportiert](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) -Methoden verwendet.'
keywords:
- DXCore, Adapter Attribut, GUIDs
topic_type:
- apiref
api_name:
- DXCore adapter attribute GUIDs
api_location:
- dxcore_interface.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a532552f144dfc21aa5d6a368aecd915d30b40c8
ms.sourcegitcommit: 8737f32d64e5f01c1d38aab92736e4088d6c446e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "106367243"
---
# <a name="dxcore-adapter-attribute-guids"></a><span data-ttu-id="3a148-104">DXCore-Adapterattribut-GUIDs</span><span class="sxs-lookup"><span data-stu-id="3a148-104">DXCore adapter attribute GUIDs</span></span>

<span data-ttu-id="3a148-105">Die folgenden Adapter Attribut-GUIDs werden in deklariert `dxcore_interface.h` und mit den [idxcoreadapterfactory:: deateadapterlist](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) -und [idxcoreadapter:: isattributesupportiert](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) -Methoden verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a148-105">The following adapter attribute GUIDs are declared in `dxcore_interface.h`, and are used with the [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) and [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) methods.</span></span> <span data-ttu-id="3a148-106">Ein oder mehrere Attribute können für einen bestimmten Adapter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="3a148-106">For any given adapter, one or more of the attributes could apply.</span></span>

| <span data-ttu-id="3a148-107">GUID</span><span class="sxs-lookup"><span data-stu-id="3a148-107">GUID</span></span> | <span data-ttu-id="3a148-108">Wert</span><span class="sxs-lookup"><span data-stu-id="3a148-108">Value</span></span> |
|-|-|
| <span data-ttu-id="3a148-109">`DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`.</span><span class="sxs-lookup"><span data-stu-id="3a148-109">`DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`.</span></span> <span data-ttu-id="3a148-110">Gibt einen Adapter an, der die Verwendung mit den [Direct3D 11](/windows/win32/direct3d11) -Grafik-APIs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a148-110">Specifies an adapter that supports being used with the [Direct3D 11](/windows/win32/direct3d11) graphics APIs.</span></span> <span data-ttu-id="3a148-111">Für bestimmte Features gibt es keine Garantien, und es besteht keine Garantie, dass das Betriebssystem in seiner aktuellen Konfiguration diese APIs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a148-111">No guarantees are made about specific features, nor is a guarantee made that the OS in its current configuration supports these APIs.</span></span> | <span data-ttu-id="3a148-112">0x8c47866b, 0x7583, 0x450d, 0xF 0, 0xF 0, 0x6b, 0xAD, 0xa8, 0x95, 0xaf, 0x4B</span><span class="sxs-lookup"><span data-stu-id="3a148-112">0x8c47866b, 0x7583, 0x450d, 0xf0, 0xf0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4b</span></span> |
| <span data-ttu-id="3a148-113">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`.</span><span class="sxs-lookup"><span data-stu-id="3a148-113">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`.</span></span> <span data-ttu-id="3a148-114">Gibt einen Adapter an, der die Verwendung mit den [Direct3D 12](/windows/win32/direct3d12) -Grafik-APIs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a148-114">Specifies an adapter that supports being used with the [Direct3D 12](/windows/win32/direct3d12) graphics APIs.</span></span> <span data-ttu-id="3a148-115">Für bestimmte Features gibt es keine Garantien, und es besteht keine Garantie, dass das Betriebssystem in seiner aktuellen Konfiguration diese APIs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a148-115">No guarantees are made about specific features, nor is a guarantee made that the OS in its current configuration supports these APIs.</span></span> | <span data-ttu-id="3a148-116">0x0c9ece4d, 0x2F 6E, 0x4F, 0x8c, 0x96, 0xe8, 0x9E, 0x33, 0x1B, 0x47, 0xb1</span><span class="sxs-lookup"><span data-stu-id="3a148-116">0x0c9ece4d, 0x2f6e, 0x4f01, 0x8c, 0x96, 0xe8, 0x9e, 0x33, 0x1b, 0x47, 0xb1</span></span> |
| <span data-ttu-id="3a148-117">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`.</span><span class="sxs-lookup"><span data-stu-id="3a148-117">`DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`.</span></span> <span data-ttu-id="3a148-118">Gibt einen Adapter an, der die Verwendung mit den [Direct3D 12 Core](../direct3d12/core-feature-levels.md) -Compute-APIs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a148-118">Specifies an adapter that supports being used with the [Direct3D 12 Core](../direct3d12/core-feature-levels.md) compute APIs.</span></span> <span data-ttu-id="3a148-119">Für bestimmte Features gibt es keine Garantien, und es besteht keine Garantie, dass das Betriebssystem in seiner aktuellen Konfiguration diese APIs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a148-119">No guarantees are made about specific features, nor is a guarantee made that the OS in its current configuration supports these APIs.</span></span> | <span data-ttu-id="3a148-120">0x248e2800, 0xa793, 0x4724, 0xAB, 0xAA, 0x23, 0xA6, 0xde, 0x1B, 0xE0, 0x90</span><span class="sxs-lookup"><span data-stu-id="3a148-120">0x248e2800, 0xa793, 0x4724, 0xab, 0xaa, 0x23, 0xa6, 0xde, 0x1b, 0xe0, 0x90</span></span> |

## <a name="requirements"></a><span data-ttu-id="3a148-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a148-121">Requirements</span></span>

| <span data-ttu-id="3a148-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a148-122">Requirement</span></span> | <span data-ttu-id="3a148-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3a148-123">Value</span></span> |
|-|-|
| <span data-ttu-id="3a148-124">Header</span><span class="sxs-lookup"><span data-stu-id="3a148-124">Header</span></span> | <span data-ttu-id="3a148-125">dxcore_interface. h</span><span class="sxs-lookup"><span data-stu-id="3a148-125">dxcore_interface.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="3a148-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a148-126">See also</span></span>

* [<span data-ttu-id="3a148-127">IDXCoreAdapterFactory::CreateAdapterList</span><span class="sxs-lookup"><span data-stu-id="3a148-127">IDXCoreAdapterFactory::CreateAdapterList</span></span>](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [<span data-ttu-id="3a148-128">IDXCoreAdapter::IsAttributeSupported</span><span class="sxs-lookup"><span data-stu-id="3a148-128">IDXCoreAdapter::IsAttributeSupported</span></span>](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [<span data-ttu-id="3a148-129">DXCore-Referenz</span><span class="sxs-lookup"><span data-stu-id="3a148-129">DXCore Reference</span></span>](./dxcore-reference.md)
* [<span data-ttu-id="3a148-130">Verwenden von DXCore zum Auflisten von Adaptern</span><span class="sxs-lookup"><span data-stu-id="3a148-130">Using DXCore to enumerate adapters</span></span>](./dxcore-enum-adapters.md)
* [<span data-ttu-id="3a148-131">Direct3D 12-Grafiken</span><span class="sxs-lookup"><span data-stu-id="3a148-131">Direct3D 12 graphics</span></span>](../direct3d12/direct3d-12-graphics.md)
