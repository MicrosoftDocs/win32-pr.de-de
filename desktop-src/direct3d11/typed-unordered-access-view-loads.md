---
title: Typisiertes Laden von ungeordneten Zugriffsansichten
description: Erfahren Sie mehr über die typisierte Last der ungeordneten Zugriffsansicht (UAV) in Direct3D 11. UAV Typed Load ist die Möglichkeit für einen Shader, aus einem UAV mit einem bestimmten DXGI_FORMAT zu lesen.
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7389ba850c68129509ca6b6a835f949dd92f5541382d9fdc2243611d409ca2a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124058"
---
# <a name="typed-unordered-access-view-loads"></a>Typisiertes Laden von ungeordneten Zugriffsansichten

Unordered Access View (UAV) Typed Load ist die Möglichkeit für einen Shader, aus einem UAV mit einem bestimmten DXGI-FORMAT zu \_ lesen.

-   [Übersicht](#overview)
-   [Unterstützte Formate und API-Aufrufe](#supported-formats-and-api-calls)
-   [Verwenden von typisierten UAV-Ladevorgängen aus HLSL](#using-typed-uav-loads-from-hlsl)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Eine ungeordnete Zugriffsansicht (UAV) ist eine Ansicht einer ungeordneten Zugriffsressource (die Puffer, Texturen und Texturarrays enthalten kann, jedoch ohne Mehrfachsampling). Ein UAV ermöglicht temporal ungeordneten Lese-/Schreibzugriff von mehreren Threads. Dies bedeutet, dass dieser Ressourcentyp von mehreren Threads gleichzeitig gelesen/geschrieben werden kann, ohne Speicherkonflikte zu generieren. Dieser gleichzeitige Zugriff wird durch die Verwendung von [Atomic Functions](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions)verarbeitet.

D3D12 und D3D11.3 erweitern die Liste der Formate, die mit typisierten UAV-Ladevorgängen verwendet werden können.

## <a name="supported-formats-and-api-calls"></a>Unterstützte Formate und API-Aufrufe

Zuvor unterstützten die folgenden drei Formate typisierte UAV-Ladevorgänge und waren für D3D11.0-Hardware erforderlich. Sie werden für alle D3D11.3- und D3D12-Hardware unterstützt.

-   R32 \_ FLOAT
-   R32 \_ UINT
-   R32 \_ SINT

Die folgenden Formate werden als Satz auf D3D12- oder D3D11.3-Hardware unterstützt. Wenn also eines unterstützt wird, werden alle unterstützt.

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

Die folgenden Formate werden optional und einzeln auf D3D12- und D3D11.3-Hardware unterstützt, sodass eine einzelne Abfrage für jedes Format durchgeführt werden muss, um die Unterstützung zu testen.

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
-   8G8 \_ SINT
-   R16 \_ UNORM
-   R16 \_ SNORM
-   R8 \_ SNORM
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

Um die Unterstützung für zusätzliche Formate zu ermitteln, rufen Sie [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) mit der [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS2-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) als ersten Parameter auf. Das `TypedUAVLoadAdditionalFormats` Bit wird festgelegt, wenn die obige Liste "supported as a set" unterstützt wird. Führen Sie einen zweiten Aufruf von **CheckFeatureSupport** aus, indem Sie eine [**D3D11 \_ FEATURE DATA FORMAT \_ \_ \_ SUPPORT2-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) verwenden (überprüfen Sie die zurückgegebene Struktur anhand des \_ \_ \_ UAV \_ TYPED LOAD-Members D3D12 FORMAT SUPPORT2 der \_ [**D3D11 \_ FORMAT \_ SUPPORT2-Enumeration),**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) um die Unterstützung in der Liste der optional unterstützten Formate oben zu ermitteln, z. B.:

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a>Verwenden von typisierten UAV-Ladevorgängen aus HLSL

Für typisierte UAVs ist das HLSL-Flag \_ D3D-SHADER \_ erfordert \_ TYPISIERTE \_ UAV-LADEFORMATE. \_ \_ \_

Hier ist ein Beispiel-Shadercode zum Verarbeiten einer typisierten UAV-Last:

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11.3-Features](direct3d-11-3-features.md)
</dt> <dt>

[Shadermodell 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 