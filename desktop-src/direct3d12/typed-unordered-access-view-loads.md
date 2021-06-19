---
title: Geladene typierte ungeordnete Zugriffsansicht (UAV)
description: Erfahren Sie mehr über die vom UAV (Unordered Access View) typierte Last in Direct3D 12. UAV Typed Load (UAV-typiertes Laden) ist die Fähigkeit eines Shaders, aus einem UAV mit einem bestimmten DXGI_FORMAT.
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128354132a58e0b8648fba2b4e1e6babb95535
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394765"
---
# <a name="typed-unordered-access-view-uav-loads"></a>Geladene typierte ungeordnete Zugriffsansicht (UAV)

Unordered Access View (UAV) Typed Load ist die Fähigkeit eines Shaders, aus einem UAV mit einem bestimmten [**DXGI-FORMAT zu \_ lesen.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

-   [Übersicht](#overview)
-   [Unterstützte Formate und API-Aufrufe](#supported-formats-and-api-calls)
-   [Verwenden von typierten UAV-Auslastungen von HLSL](#using-typed-uav-loads-from-hlsl)
-   [Verwenden von UNORM- und SNORM-typisierten UAV-Lasten von HLSL](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [Verwandte Themen](#related-topics)

## <a name="overview"></a>Übersicht

Eine ungeordnete Zugriffsansicht (UAV) ist eine Ansicht einer ungeordneten Zugriffsressource (die Puffer, Texturen und Texturarrays enthalten kann, jedoch ohne Mehrfachstichproben). Ein UAV ermöglicht den zeitlich ungeordneten Lese-/Schreibzugriff von mehreren Threads. Dies bedeutet, dass dieser Ressourcentyp gleichzeitig von mehreren Threads gelesen/geschrieben werden kann, ohne Arbeitsspeicherkonflikte zu generieren. Dieser gleichzeitige Zugriff wird mithilfe von [Atomic Functions verarbeitet.](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions)

D3D12 (und D3D11.3) erweitert die Liste der Formate, die mit typierten UAV-Auslastungen verwendet werden können.

## <a name="supported-formats-and-api-calls"></a>Unterstützte Formate und API-Aufrufe

Zuvor unterstützten die folgenden drei Formate typierte UAV-Auslastungen und waren für D3D11.0-Hardware erforderlich. Sie werden für alle D3D11.3- und D3D12-Hardware unterstützt.

-   R32 \_ FLOAT
-   R32 \_ UINT
-   R32 \_ SINT

Die folgenden Formate werden als Set auf D3D12- oder D3D11.3-Hardware unterstützt. Wenn also eins unterstützt wird, werden alle unterstützt.

-   R32G32B32A32 \_ FLOAT
-   R32G32B32A32 \_ UINT
-   R32G32B32A32 \_ SINT
-   R16G16B16A16 \_ FLOAT
-   R16G16B16A16 \_ UINT
-   R16G16B16A16 \_ SINT
-   R8G8B8A8 \_ UNORM
-   R8G8B8A8 \_ UINT
-   R8G8B8A8 \_ SINT
-   R16 \_ FLOAT
-   R16 \_ UINT
-   R16 \_ SINT
-   R8 \_ UNORM
-   R8 \_ UINT
-   R8 \_ SINT

Die folgenden Formate werden optional und einzeln auf D3D12- und D3D11.3-Hardware unterstützt, sodass für jedes Format eine einzelne Abfrage durchgeführt werden muss, um die Unterstützung zu testen.

-   R16G16B16A16 \_ UNORM
-   R16G16B16A16 \_ SNORM
-   R32G32 \_ FLOAT
-   R32G32 \_ UINT
-   R32G32 \_ SINT
-   R10G10B10A2 \_ UNORM
-   R10G10B10A2 \_ UINT
-   R11G11B10 \_ FLOAT
-   R8G8B8A8 \_ SNORM
-   R16G16 \_ FLOAT
-   R16G16 \_ UNORM
-   R16G16 \_ UINT
-   R16G16 \_ SNORM
-   R16G16 \_ SINT
-   R8G8 \_ UNORM
-   R8G8 \_ UINT
-   R8G8 \_ SNORM
-   R8G8 \_ SINT
-   R16 \_ UNORM
-   R16 \_ SNORM
-   R8 \_ SNORM
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Um die Unterstützung für zusätzliche Formate zu ermitteln, rufen Sie [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) mit der [**D3D12 \_ FEATURE DATA \_ \_ D3D12 \_ OPTIONS-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) als ersten Parameter auf (siehe [Capability Querying](capability-querying.md)). Das *Feld TypedUAVLoadAdditionalFormats* wird festgelegt, wenn die obige Liste "Supported as a set" unterstützt wird. Führen Sie einen zweiten Aufruf von **CheckFeatureSupport** mithilfe einer [**D3D12 \_ FEATURE DATA FORMAT \_ \_ \_ SUPPORT-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) durch (überprüfen Sie die zurückgegebene Struktur anhand des \_ \_ \_ UAV \_ TYPED LOAD-Members \_ [**D3D12 \_ FORMAT \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) in der Liste der oben aufgeführten optional unterstützten Formate, z. B.:

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a>Verwenden von typierten UAV-Auslastungen von HLSL

Für typierte UAVs ist das HLSL-Flag \_ D3D-SHADER \_ ERFORDERT \_ TYPIERTE \_ \_ UAV-LADE \_ ZUSÄTZLICHE \_ FORMATE.

Hier ist ein Shader-Beispielcode zum Verarbeiten einer typierten UAV-Last:

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a>Verwenden von UNORM- und SNORM-typisierten UAV-Lasten von HLSL

Wenn Sie typisiert UAV-Lasten zum Lesen aus einer UNORM- oder SNORM-Ressource verwenden, müssen Sie den Elementtyp des HLSL-Objekts ordnungsgemäß als oder `unorm` `snorm` deklarieren. Es wird als nicht definiertes Verhalten angegeben, um einen Konflikt zwischen dem in HLSL deklarierten Elementtyp und dem zugrunde liegenden Ressourcendatentyp zu vermeiden. Wenn Sie beispielsweise typisiert UAV-Lasten für eine Pufferressource mit R8-UNORM-Daten verwenden, müssen Sie den Elementtyp als \_ `unorm float` deklarieren:

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Darstellung](rendering.md)
</dt> <dt>

[Ressourcenbindung](resource-binding.md)
</dt> <dt>

[Ressourcenbindung in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Shadermodell 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Festlegen von Stammsignaturen in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 