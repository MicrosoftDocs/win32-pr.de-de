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
# <a name="capability-querying"></a>Funktions Abfrage

Die Anwendung kann den Grad der Unterstützung für die Ressourcen Bindung (sowie die Ebene der Unterstützung vieler anderer Features) mit einem [**ID3D12Device:: checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)-Befehl ermitteln.

## <a name="how-to-query-for-the-resource-binding-tier"></a>Abfragen der Ressourcen Bindungs Ebene

Dieses erste Beispiel konzentriert sich auf die Ressourcen Bindung. Jede Ressourcen Bindungs Ebene ist eine übergeordnete Gruppe von niedrigeren Funktionsebenen, sodass der Code, der auf einer bestimmten Ebene funktioniert, auf jeder höheren Ebene unverändert funktioniert.

Die Ressourcen Bindungs Ebenen sind Konstanten in der [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) -Enumeration.

Um die Ressourcen Bindungs Ebene abzufragen, verwenden Sie Code wie diesen. In diesem Codebeispiel wird das allgemeine Muster für die Abfrage der verschiedenen Arten von Featureunterstützung veranschaulicht.

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

Beachten Sie, dass jede Enumerationskonstante, die Sie übergeben (in diesem Fall [**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)), über eine entsprechende Datenstruktur verfügt, die Informationen über diese Funktion oder eine Reihe von Features empfängt (in diesem Fall [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)). Übergeben Sie immer einen Zeiger an die-Struktur, die mit der von Ihnen übergebenen Enumerationskonstante übereinstimmt.

## <a name="how-to-query-for-any-feature-level"></a>Abfragen für Funktionsebenen

Ebenso wie die Ressourcen Bindungs Ebene gibt es viele weitere Features, deren Unterstützungs Ebene Sie mithilfe des gleichen Musters Abfragen können, das im obigen Codebeispiel gezeigt wird. Sie übergeben einfach eine andere Konstante von der [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) -Enumeration an [**ID3D12Device:: checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (um der API mitzuteilen, welche Funktion Support Informationen anfordern soll) und übergeben einen Zeiger auf eine Instanz der übereinstimmenden Struktur (in der die angeforderten Informationen empfangen werden sollen).

- Übergeben Sie **D3D12_FEATURE_ARCHITECTURE** und [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).
- Übergeben Sie **D3D12_FEATURE_ARCHITECTURE1** und [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).
- Übergeben Sie **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** und [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).
- Übergeben Sie **D3D12_FEATURE_CROSS_NODE** und [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).
- Übergeben Sie **D3D12_FEATURE_D3D12_OPTIONS** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).
- Übergeben Sie **D3D12_FEATURE_D3D12_OPTIONS1** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).
- Übergeben Sie **D3D12_FEATURE_D3D12_OPTIONS2** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).
- Übergeben Sie **D3D12_FEATURE_D3D12_OPTIONS3** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).
- Übergeben Sie **D3D12_FEATURE_D3D12_OPTIONS4** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).
- Übergeben Sie **D3D12_FEATURE_D3D12_OPTIONS5** und [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).
- Übergeben Sie **D3D12_FEATURE_EXISTING_HEAPS** und [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).
- Übergeben Sie **D3D12_FEATURE_FEATURE_LEVELS** und [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).
- Übergeben Sie **D3D12_FEATURE_FORMAT_INFO** und [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).
- Übergeben Sie **D3D12_FEATURE_FORMAT_SUPPORT** und [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).
- Übergeben Sie **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** und [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).
- Übergeben Sie **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** und [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).
- Übergeben Sie **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** und [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).
- Übergeben Sie **D3D12_FEATURE_ROOT_SIGNATURE** und [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).
- Übergeben Sie **D3D12_FEATURE_SERIALIZATION** und [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).
- Übergeben Sie **D3D12_FEATURE_SHADER_CACHE** und [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).
- Übergeben Sie **D3D12_FEATURE_SHADER_MODEL** und [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).

## <a name="hardware-support-for-dxgi-formats"></a>Hardware Unterstützung für DXGI-Formate

Weitere Informationen zum Anzeigen von Tabellen mit DXGI-Formaten und Hardware Features finden Sie in den folgenden Themen.

- [DXGI-Format Unterstützung für Direct3D Featureebene 12,1 Hardware](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [DXGI-Format Unterstützung für Direct3D Featureebene 12,0 Hardware](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [DXGI-Format Unterstützung für Direct3D Featureebene 11,1 Hardware](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [DXGI-Format Unterstützung für Direct3D Featureebene 11,0 Hardware](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- [Hardware Unterstützung für Direct3D 10level9-Formate](/previous-versions//ff471324(v=vs.85))
- [Hardware Unterstützung für Direct3D 10,1-Formate](/previous-versions//cc627091(v=vs.85))
- [Hardware Unterstützung für Direct3D 10-Formate](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>Verwandte Themen

* [Ressourcenbindung in Direct3D 12](resource-binding.md)
* [Hardware Funktionsebenen](hardware-feature-levels.md)
* [Stamm Signaturen](root-signatures.md)