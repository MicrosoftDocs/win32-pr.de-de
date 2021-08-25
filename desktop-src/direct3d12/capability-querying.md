---
title: Funktionsabfragen
description: 'Ihre Anwendung kann mithilfe eines Aufrufs von ID3D12Device \: CheckFeatureSupport den Grad der Unterstützung für die Ressourcenbindung und viele \: andere Features entdecken.'
ms.assetid: ECBAF8EF-5D91-46D8-9D6E-A7FA4203B9F8
ms.date: 11/26/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: a99174515883f8995167a7b866ab1ef8b77b56f7a0be2bb83f960abd06e47713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851400"
---
# <a name="capability-querying"></a>Funktionsabfragen

Ihre Anwendung kann mithilfe eines Aufrufs von [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)den Grad der Unterstützung für die Ressourcenbindung (sowie den Grad der Unterstützung für viele andere Features) feststellen.

## <a name="how-to-query-for-the-resource-binding-tier"></a>Abfragen der Ressourcenbindungsebene

Dieses erste Beispiel konzentriert sich auf die Ressourcenbindung. Jede Ressourcenbindungsebene ist eine Obermenge von niedrigeren Ebenen in der Funktionalität, sodass Code, der auf einer bestimmten Ebene funktioniert, auf jeder höheren Ebene unverändert funktioniert.

Die Ressourcenbindungsebenen sind Konstanten in [**der**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) D3D12_RESOURCE_BINDING_TIER Enumeration.

Verwenden Sie code wie diesen, um die Ressourcenbindungsebene abfragen zu können. In diesem Codebeispiel wird das allgemeine Muster zum Abfragen einer der verschiedenen Arten von Featureunterstützung veranschaulicht.

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

Beachten Sie, dass jede aufzählte Konstante, die Sie übergeben (in diesem Fall [**D3D12_FEATURE_D3D12_OPTIONS),**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)über eine entsprechende Datenstruktur verfügt, die Informationen über dieses Feature oder eine Gruppe von Features empfängt ([**in**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)diesem Fall D3D12_FEATURE_DATA_D3D12_OPTIONS). Übergeben Sie immer einen Zeiger auf die -Struktur, die der aufzählten Konstanten entspricht, die Sie übergeben.

## <a name="how-to-query-for-any-feature-level"></a>Abfragen einer beliebigen Funktionsebene

Neben der Ressourcenbindungsebene gibt es viele weitere Features, deren Unterstützungsebene Sie abfragen können, indem Sie das gleiche Muster wie im obigen Codebeispiel verwenden. Sie übergeben einfach eine andere Konstante als die [**D3D12_FEATURE-Enumeration**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) an [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (um der API mitteilen zu können, für welches Feature Supportinformationen angefordert werden sollen) und übergeben einen Zeiger auf eine Instanz der übereinstimmenden Struktur (in der die angeforderten Informationen empfangen werden sollen).

- Übergeben **D3D12_FEATURE_ARCHITECTURE** und [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).
- Übergeben **D3D12_FEATURE_ARCHITECTURE1** und [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).
- Übergeben **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** und [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).
- Übergeben **D3D12_FEATURE_CROSS_NODE** und [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).
- Übergeben **D3D12_FEATURE_D3D12_OPTIONS** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).
- Übergeben **D3D12_FEATURE_D3D12_OPTIONS1** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).
- Übergeben **D3D12_FEATURE_D3D12_OPTIONS2** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).
- Übergeben **D3D12_FEATURE_D3D12_OPTIONS3** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).
- Übergeben **D3D12_FEATURE_D3D12_OPTIONS4** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).
- Übergeben **D3D12_FEATURE_D3D12_OPTIONS5** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).
- Übergeben **D3D12_FEATURE_EXISTING_HEAPS** und [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).
- Übergeben **D3D12_FEATURE_FEATURE_LEVELS** und [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).
- Übergeben **D3D12_FEATURE_FORMAT_INFO** und [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).
- Übergeben **D3D12_FEATURE_FORMAT_SUPPORT** und [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).
- Übergeben **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** und [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).
- Übergeben **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** und [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).
- Übergeben **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** und [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).
- Übergeben **D3D12_FEATURE_ROOT_SIGNATURE** und [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).
- Übergeben **D3D12_FEATURE_SERIALIZATION** und [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).
- Übergeben **D3D12_FEATURE_SHADER_CACHE** und [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).
- Übergeben **D3D12_FEATURE_SHADER_MODEL** und [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).

## <a name="hardware-support-for-dxgi-formats"></a>Hardwareunterstützung für DXGI-Formate

Tabellen mit DXGI-Formaten und Hardwarefeatures finden Sie in diesen Themen.

- [DXGI-Formatunterstützung für Direct3D-Hardware auf Featureebene 12.1](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [DXGI-Formatunterstützung für Direct3D-Hardware auf Featureebene 12.0](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [DXGI-Formatunterstützung für Direct3D-Hardware auf Featureebene 11.1](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [DXGI-Formatunterstützung für Direct3D-Hardware auf Featureebene 11.0](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- [Hardwareunterstützung für Direct3D 10Level9-Formate](/previous-versions//ff471324(v=vs.85))
- [Hardwareunterstützung für Direct3D 10.1-Formate](/previous-versions//cc627091(v=vs.85))
- [Hardwareunterstützung für Direct3D 10-Formate](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Zugehörige Themen

* [Ressourcenbindung in Direct3D 12](resource-binding.md)
* [Hardwarefeatureebenen](hardware-feature-levels.md)
* [Stammsignaturen](root-signatures.md)