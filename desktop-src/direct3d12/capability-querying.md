---
title: Funktions Abfrage
description: 'Die Anwendung kann den Grad der Unterstützung für die Ressourcen Bindung und viele weitere Features mit einem ID3D12Device \: \: checkfeaturesupport-Vorgang ermitteln.'
ms.assetid: ECBAF8EF-5D91-46D8-9D6E-A7FA4203B9F8
ms.date: 11/26/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: eaf451f91d51cfa6e900f328898c3418f0974a2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548662"
---
# <a name="capability-querying"></a><span data-ttu-id="6a9c8-103">Funktions Abfrage</span><span class="sxs-lookup"><span data-stu-id="6a9c8-103">Capability querying</span></span>

<span data-ttu-id="6a9c8-104">Die Anwendung kann den Grad der Unterstützung für die Ressourcen Bindung (sowie die Ebene der Unterstützung vieler anderer Features) mit einem [**ID3D12Device:: checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)-Befehl ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6a9c8-104">Your application can discover the level of support for resource binding (as well as the level of support for many other features), with a call to [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

## <a name="how-to-query-for-the-resource-binding-tier"></a><span data-ttu-id="6a9c8-105">Abfragen der Ressourcen Bindungs Ebene</span><span class="sxs-lookup"><span data-stu-id="6a9c8-105">How to query for the resource binding tier</span></span>

<span data-ttu-id="6a9c8-106">Dieses erste Beispiel konzentriert sich auf die Ressourcen Bindung.</span><span class="sxs-lookup"><span data-stu-id="6a9c8-106">This first example focuses on resource binding.</span></span> <span data-ttu-id="6a9c8-107">Jede Ressourcen Bindungs Ebene ist eine übergeordnete Gruppe von niedrigeren Funktionsebenen, sodass der Code, der auf einer bestimmten Ebene funktioniert, auf jeder höheren Ebene unverändert funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6a9c8-107">Each resource binding tier is a superset of lower tiers in functionality, so code that works on a given tier works unchanged on any higher tier.</span></span>

<span data-ttu-id="6a9c8-108">Die Ressourcen Bindungs Ebenen sind Konstanten in der [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="6a9c8-108">The resource binding tiers are constants in the [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) enumeration.</span></span>

<span data-ttu-id="6a9c8-109">Um die Ressourcen Bindungs Ebene abzufragen, verwenden Sie Code wie diesen.</span><span class="sxs-lookup"><span data-stu-id="6a9c8-109">To query for the resource binding tier, use code such as this.</span></span> <span data-ttu-id="6a9c8-110">In diesem Codebeispiel wird das allgemeine Muster für die Abfrage der verschiedenen Arten von Featureunterstützung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6a9c8-110">This code example demonstrates the general pattern for querying for any of the various kinds of feature support.</span></span>

```cppwinrt
D3D12_RESOURCE_BINDING_TIER get_resource_binding_tier(::ID3D12Device* pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &featureSupport, sizeof(featureSupport))
    );

    switch (featureSupport.ResourceBindingTier)
    {
    case D3D12_RESOURCE_BINDING_TIER_1:
        // Tier 1 is supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_2:
        // Tiers 1 and 2 are supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_3:
        // Tiers 1, 2, and 3 are supported.
        break;
    }

    return featureSupport.ResourceBindingTier;
}
```

<span data-ttu-id="6a9c8-111">Beachten Sie, dass jede Enumerationskonstante, die Sie übergeben (in diesem Fall [**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)), über eine entsprechende Datenstruktur verfügt, die Informationen über diese Funktion oder eine Reihe von Features empfängt (in diesem Fall [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-111">Note that any enumerated constant that you pass ([**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature), in this case) has a corresponding data structure that receives info about that feature or set of features ([**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options), in this case).</span></span> <span data-ttu-id="6a9c8-112">Übergeben Sie immer einen Zeiger an die-Struktur, die mit der von Ihnen übergebenen Enumerationskonstante übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="6a9c8-112">Always pass a pointer to the structure that matches the enumerated constant that you pass.</span></span>

## <a name="how-to-query-for-any-feature-level"></a><span data-ttu-id="6a9c8-113">Abfragen für Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="6a9c8-113">How to query for any feature level</span></span>

<span data-ttu-id="6a9c8-114">Ebenso wie die Ressourcen Bindungs Ebene gibt es viele weitere Features, deren Unterstützungs Ebene Sie mithilfe des gleichen Musters Abfragen können, das im obigen Codebeispiel gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6a9c8-114">As well as the resource binding tier, there are many other features whose level of support you can query for using the same pattern shown in the code example above.</span></span> <span data-ttu-id="6a9c8-115">Sie übergeben einfach eine andere Konstante von der [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) -Enumeration an [**ID3D12Device:: checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (um der API mitzuteilen, welche Funktion Support Informationen anfordern soll) und übergeben einen Zeiger auf eine Instanz der übereinstimmenden Struktur (in der die angeforderten Informationen empfangen werden sollen).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-115">You just pass a different constant from the [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) enumeration to [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (to tell the API what feature to request support information on), and you pass a pointer to an instance of the matching structure (in which to receive the requested info).</span></span>

- <span data-ttu-id="6a9c8-116">Übergeben Sie **D3D12_FEATURE_ARCHITECTURE** und [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-116">Pass **D3D12_FEATURE_ARCHITECTURE** and [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).</span></span>
- <span data-ttu-id="6a9c8-117">Übergeben Sie **D3D12_FEATURE_ARCHITECTURE1** und [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-117">Pass **D3D12_FEATURE_ARCHITECTURE1** and [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).</span></span>
- <span data-ttu-id="6a9c8-118">Übergeben Sie **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** und [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-118">Pass **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** and [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).</span></span>
- <span data-ttu-id="6a9c8-119">Übergeben Sie **D3D12_FEATURE_CROSS_NODE** und [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-119">Pass **D3D12_FEATURE_CROSS_NODE** and [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).</span></span>
- <span data-ttu-id="6a9c8-120">Übergeben Sie **D3D12_FEATURE_D3D12_OPTIONS** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-120">Pass **D3D12_FEATURE_D3D12_OPTIONS** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).</span></span>
- <span data-ttu-id="6a9c8-121">Übergeben Sie **D3D12_FEATURE_D3D12_OPTIONS1** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-121">Pass **D3D12_FEATURE_D3D12_OPTIONS1** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).</span></span>
- <span data-ttu-id="6a9c8-122">Übergeben Sie **D3D12_FEATURE_D3D12_OPTIONS2** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-122">Pass **D3D12_FEATURE_D3D12_OPTIONS2** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).</span></span>
- <span data-ttu-id="6a9c8-123">Übergeben Sie **D3D12_FEATURE_D3D12_OPTIONS3** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-123">Pass **D3D12_FEATURE_D3D12_OPTIONS3** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).</span></span>
- <span data-ttu-id="6a9c8-124">Übergeben Sie **D3D12_FEATURE_D3D12_OPTIONS4** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-124">Pass **D3D12_FEATURE_D3D12_OPTIONS4** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).</span></span>
- <span data-ttu-id="6a9c8-125">Übergeben Sie **D3D12_FEATURE_D3D12_OPTIONS5** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-125">Pass **D3D12_FEATURE_D3D12_OPTIONS5** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).</span></span>
- <span data-ttu-id="6a9c8-126">Übergeben Sie **D3D12_FEATURE_EXISTING_HEAPS** und [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-126">Pass **D3D12_FEATURE_EXISTING_HEAPS** and [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).</span></span>
- <span data-ttu-id="6a9c8-127">Übergeben Sie **D3D12_FEATURE_FEATURE_LEVELS** und [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-127">Pass **D3D12_FEATURE_FEATURE_LEVELS** and [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).</span></span>
- <span data-ttu-id="6a9c8-128">Übergeben Sie **D3D12_FEATURE_FORMAT_INFO** und [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-128">Pass **D3D12_FEATURE_FORMAT_INFO** and [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).</span></span>
- <span data-ttu-id="6a9c8-129">Übergeben Sie **D3D12_FEATURE_FORMAT_SUPPORT** und [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-129">Pass **D3D12_FEATURE_FORMAT_SUPPORT** and [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).</span></span>
- <span data-ttu-id="6a9c8-130">Übergeben Sie **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** und [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-130">Pass **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** and [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).</span></span>
- <span data-ttu-id="6a9c8-131">Übergeben Sie **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** und [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-131">Pass **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** and [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).</span></span>
- <span data-ttu-id="6a9c8-132">Übergeben Sie **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** und [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-132">Pass **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** and [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).</span></span>
- <span data-ttu-id="6a9c8-133">Übergeben Sie **D3D12_FEATURE_ROOT_SIGNATURE** und [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-133">Pass **D3D12_FEATURE_ROOT_SIGNATURE** and [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).</span></span>
- <span data-ttu-id="6a9c8-134">Übergeben Sie **D3D12_FEATURE_SERIALIZATION** und [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-134">Pass **D3D12_FEATURE_SERIALIZATION** and [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).</span></span>
- <span data-ttu-id="6a9c8-135">Übergeben Sie **D3D12_FEATURE_SHADER_CACHE** und [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-135">Pass **D3D12_FEATURE_SHADER_CACHE** and [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).</span></span>
- <span data-ttu-id="6a9c8-136">Übergeben Sie **D3D12_FEATURE_SHADER_MODEL** und [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).</span><span class="sxs-lookup"><span data-stu-id="6a9c8-136">Pass **D3D12_FEATURE_SHADER_MODEL** and [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).</span></span>

## <a name="hardware-support-for-dxgi-formats"></a><span data-ttu-id="6a9c8-137">Hardware Unterstützung für DXGI-Formate</span><span class="sxs-lookup"><span data-stu-id="6a9c8-137">Hardware support for DXGI Formats</span></span>

<span data-ttu-id="6a9c8-138">Weitere Informationen zum Anzeigen von Tabellen mit DXGI-Formaten und Hardware Features finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="6a9c8-138">To view tables of DXGI formats and hardware features, refer to these topics.</span></span>

- [<span data-ttu-id="6a9c8-139">DXGI-Format Unterstützung für Direct3D Featureebene 12,1 Hardware</span><span class="sxs-lookup"><span data-stu-id="6a9c8-139">DXGI Format Support for Direct3D Feature Level 12.1 Hardware</span></span>](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [<span data-ttu-id="6a9c8-140">DXGI-Format Unterstützung für Direct3D Featureebene 12,0 Hardware</span><span class="sxs-lookup"><span data-stu-id="6a9c8-140">DXGI Format Support for Direct3D Feature Level 12.0 Hardware</span></span>](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [<span data-ttu-id="6a9c8-141">DXGI-Format Unterstützung für Direct3D Featureebene 11,1 Hardware</span><span class="sxs-lookup"><span data-stu-id="6a9c8-141">DXGI Format Support for Direct3D Feature Level 11.1 Hardware</span></span>](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [<span data-ttu-id="6a9c8-142">DXGI-Format Unterstützung für Direct3D Featureebene 11,0 Hardware</span><span class="sxs-lookup"><span data-stu-id="6a9c8-142">DXGI Format Support for Direct3D Feature Level 11.0 Hardware</span></span>](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- <span data-ttu-id="6a9c8-143">[Hardware Unterstützung für Direct3D 10level9-Formate](/previous-versions//ff471324(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a9c8-143">[Hardware Support for Direct3D 10Level9 Formats](/previous-versions//ff471324(v=vs.85))</span></span>
- <span data-ttu-id="6a9c8-144">[Hardware Unterstützung für Direct3D 10,1-Formate](/previous-versions//cc627091(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a9c8-144">[Hardware Support for Direct3D 10.1 Formats](/previous-versions//cc627091(v=vs.85))</span></span>
- <span data-ttu-id="6a9c8-145">[Hardware Unterstützung für Direct3D 10-Formate](/previous-versions//cc627090(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a9c8-145">[Hardware Support for Direct3D 10 Formats](/previous-versions//cc627090(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a9c8-146">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6a9c8-146">Related topics</span></span>

* [<span data-ttu-id="6a9c8-147">Ressourcenbindung in Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="6a9c8-147">Resource binding in Direct3D 12</span></span>](resource-binding.md)
* [<span data-ttu-id="6a9c8-148">Hardware Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="6a9c8-148">Hardware feature levels</span></span>](hardware-feature-levels.md)
* [<span data-ttu-id="6a9c8-149">Stamm Signaturen</span><span class="sxs-lookup"><span data-stu-id="6a9c8-149">Root signatures</span></span>](root-signatures.md)